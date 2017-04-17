# Publication Extraction Web Data View Chrome Extension
This is a subproject of Web Data View project, where you can visually select an area of publication text, or highlight the text, and then the Chrome extension will automatically organize the data into a web table, which can be copied to clipboard, or exported as an Excel file. The Chrome extension only works on publication domain but the key technique can be adapted to other domains such as shopping, social media, etc. Our ultimate goal is to enable web browsers to not only present but also understand web pages.

Download the code from this page and follow the guildline [here](https://wiki.illinois.edu/wiki/download/attachments/586662115/WebDataViewInstallationGuide.pdf?version=2&modificationDate=1465568899000&api=v2) to install Web Data View Chrome extension. Please use the code from this repository instead of the zip file mentioned in the guide, because it is more updated.

An example webpage to test: http://www.forwarddatalab.org/publications

A few screenshots to demonstrate how it works: https://www.dropbox.com/s/hh06xayo8wvuz8r/Web%20Data%20View%20Demo.pdf?dl=0

You can test the Chrome extension on your own by installing the extension and do the following steps:
* Note: for the current version, we recommend using "Extract Publications From Highlighted Text" functionality as it is more stable than the remaining choice. The guideline below uses that functionality.
* Highlight the publication text you want to extract. You can highlight one or more citations, but each citation must be complete. 
* Click on the WDV button at the top right corner of your Chrome browser, and then click on button "Extract Publications From Highlighted Text"
* There will be an alert showing the text you highlighted. You should click "OK" to dismiss the alert.
* The extraction will take about 8-15 seconds for less than 10 citations, so please be patient.
* After the extraction is done, a table will pop up.
* You can click on "Copy" button at the top of the pop-up window to copy the data to clipboard, which can be pasted to anywhere like Excel.
* You can also select a few constraints that we suggested at the bottom of the pop-up window, and then click on button "Enforce constraints selected below" to enforce the constraints. The constraint enforcement may take 10 seconds to finish.
* You can also right click to any column to let our system know that such field should not exist. After the right click, you will see a red constraint in the list of constraints, which writes something like "title does not appear". After adding the constraint, you can also click on button "Enforce constraints selected below" to enforce it, and the system will move content from that field to other fields.

Please note that our Chrome extension at this moment can operate only on non-HTTPS page. Most UIUC professor publication pages use non-HTTPS, but it is not the cases for other universities like UMass, UIC, etc. Finally, besides the Chrome extension, we run a server which actually runs the data extraction algorithm, i.e., a modified version of Conditional Random Field. The server code is not published yet, but you can contact me at ltpham3 at illinois dot edu to ask for the server code.
