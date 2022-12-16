# NWEA Roster Validation Error Tool
Spreadsheet tool which assists in identify the cause of errors found during the roster import.

## About
Spreadsheet tool which can greatly assist with identifying the cause of validation errors which the system identified.  It purely uses advanced spreadsheet functions in order to avoid security concerns and installation issues.
>

## Getting Started
Simply download the spreadsheet, open in MS Excel, then follow the instructions.

## Usage
1. After attempting to import and recieving the Valdiation error notice, export the errors to file.
2. Prior to using this tool, create a backup copy of your roster file.
3. Place your roster file in the same directory/folder as the Roster Validation Error (RVE) spreadsheet tool.  
4. Open both the RVE and the roster file.  Both of the spreadsheets must remain open at the same time.
5. Open the 'Export - File Validation Errors.csv' from step 1 and copy (ctrl-c) the errors (up to 50)
	1. The errors are located from A thru E columns
	2. Do not include the error file heading (row 1) when copying the errors
6. In the RVE select the 'Errors' tab, click on B3, then paste the errors from step 5.
7. Select the Dashboard (DB) tab and ensure the roster filename is entered correctly near the top
7. Follow the guidance to identify issues and correct the errors
8. After correcting an error, switch to the 'Error' tab and remove the "RF" (or entire entry) for the error
	1. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/NextError.png" width="80%" />
9. Switch back to the DB tab and the next error will be shown
10. Continue the process until all errors are corrected
11. Once all errors are corrected, or if you would like to check on your progress, save the roster file and import again
12. Although not common, new errors may appear after correcting all the previous errors.
	1. Once an error is found in set or row, the system may not continue to another set of checks.  After correcting an error, it could then find another error in the same set or row.