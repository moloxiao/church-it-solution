This page introduces a case study of an implementation and the main steps of each stage.  
The following solution is based on the Google technology stack, making it easy to manage your website using tools like Google Sheets and Google Calendar.  

## Day1
In this step, ensure that visiting xxx.com directs users to your website :  
|  task   | Person in charge  | Estimated Time| Description| 
|  ----  | ----  | ----| -------- |
| **Prepare website templates**  | service provider | NA | Show you the basic structure of the website |
| **register a domain name**  | you | 5~10min | |
| **configure the domain name** | you & service provider| 5~10 min |Complete the necessary configurations to ensure the domain points to the demonstration website |

You can now access your website, and we will start taking over the management functions.  
|  task   | Person in charge  | Estimated Time| Description| 
|  ----  | ----  | ---- | -------- |
| **google calendar**  | you & service provider |5~10min |  |
| **google sheet**  | you & service provider |5~10min | |
| **google slide** | you & service provider |5~10min | |

### Tip 1 - google sheet
Here's the step-by-step guide in English on how to use Google Apps Script to share Google Sheets data in JSON format.   
1. **Create a Google Apps Script Project**

Open your Google Sheets document.  
Click on Extensions -> Apps Script.  
  
2. **Write the Google Apps Script Code**  

In the Apps Script editor, delete any existing code and add the following code:  
```
function doGet(e) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  var data = sheet.getDataRange().getValues();
  var jsonData = JSON.stringify(data);
  return ContentService.createTextOutput(jsonData).setMimeType(ContentService.MimeType.JSON);
}
```

This script reads the data from the active sheet and returns it in JSON format.

3. **Deploy the Script as a Web App**

Click on Deploy -> New deployment.  
In the Select type dropdown, choose Web app.  
Under Who has access, select Anyone or Anyone with the link.  
Click Deploy.  
Authorize the script by following the prompts to allow necessary permissions.  
After deployment, copy the web app URL provided.  

### Tip 2 -  google calendar
  
### Tip 3 - google slide
