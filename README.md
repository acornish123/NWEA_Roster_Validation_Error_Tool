# NWEA Roster Validation Error Tool
Spreadsheet tool which assists in identify the cause of errors found during the roster import.

## About
Spreadsheet tool which can greatly assist with identifying the cause of validation errors which the system identified.  It purely uses advanced spreadsheet functions in order to avoid security concerns and installation issues.  Partners do not have to install any programs, accept any warnings, or make any changes to security settings to use the tool.  
This file is only for assisting with locating the cause of errors which were detected during an import.  It does not detect errors on its own, instead it utilizes the errors copied from the associated 'Export - File Validation Errors.csv' to display helpful information concerning each particular error.

## REQUIREMENTS

Currently the tool only works in Microsoft Excel.  It has been tested in Office 365, though other current versions of Excel should work also.
It is expected that versions for other popular spreadsheet programs, such as Mac Numbers, could be created.


## TODO

Although the tool is working there is much still needing to be accomplished.
1. Currently works only with Microsoft Excel.  Need verify MS Excel version compatibility and create versions for other popular spreadsheet programs.
2. Add handling for errors generated from optional columns.
3. Improve User Interface
4. Simplify setup process or provide video guidance.  Process appears complicated but can be done in less than a minute.
5. Add process for choosing error from Dashboard.

## Getting Started
Download the spreadsheet, open in MS Excel, then follow the instructions.

## Usage

### Setup
1. After attempting to import and receiving the validation error notice, export the errors to file.
2. Prior to using this tool, create a backup copy of your roster file.
3. Place your roster file in the same directory/folder as the Roster Validation Error (RVE) spreadsheet tool. 
4. Open both the RVE and the roster file.  Both of these spreadsheets must remain open to use the tool.
5. Open the 'Export - File Validation Errors.csv' from step 1 and copy (ctrl-c) the errors (up to 50)
	1. The errors are located from A thru E columns
	2. Do not include the error file heading (row 1) when copying the errors
6. In the RVE select the 'Errors' tab, click on cell B3, then paste the errors from step 5.
7. Select the Dashboard (DB) tab and ensure the roster filename is entered correctly near the top
8. The first error should now be displayed in the Dashboard

### Correcting errors
1. Use the displayed data to identify issues and correct the errors
 	1. See [Step 7](#dashboard-step) in the ['Walk thru Example'](#walk-through-example) for additional guidance.
2. After correcting an error, switch to the 'Error' tab and remove the "RF" (or entire entry) for the error
	1. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/NextError.png" width="80%" />
3. Switch back to the DB tab and the next error will be shown
4. Continue the process until all errors are corrected
5. Once all errors are corrected, or if you would like to check on your progress, save the roster file and import again
6. Although not common, new errors may appear after correcting all the previous errors.
	1. Once an error is found in set or row, the system may not continue to another set of checks.  After correcting an error, it could then find another error in the same set or row.
	
## Walk through example

1. Download the three spreadsheet files from the repo in to a single folder
	1. exRoster.csv
	2. Export - File Validation Errors.csv 
	3. RosterValidationErrorTool.xlsx
2. Open the 'RosterValidationErrorTool.xlsx' (RVE)
	1. The Roster Filename in B2 should contain 'exRoster'.  If it does not, enter the correct filename in B2.
	2. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/001-openTool.png" width="50%" />
3. Open the 'exRoster.csv' in a separate Excel window
	1. The 'ERRONEOUOS DATA MISSING' error occurs because the 'Errors' have not been entered		
	2. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/002-openRoster.png" width="50%" />
4. Open the 'Export - File Validation Errors.csv'
5. Copy the errors from the file to the 'Errors' tab in the RVE
	1. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/003-copyErrors.png" width="80%" />
	2. The first error should be highlighted, if you copied over the header from the error file, delete the data from B3 or the entire row
	3. Close the 'Export - File Validation Errors.csv' window.
6. Switch back to the 'Dashboard' tab.
	1. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/004-dbFullError.png" width="50%" />
7. <a name="dashboard-step"></a>The Dashboard now displays information about the error
	1. Information directly from the error
		1. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/005-errorInfo.png" width="50%" />
	2. Suggestion(s) or information about the error
		1. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/006-suggestions.png" width="50%" />
	3. Data from the roster related to the error
		1. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/007-dataFromRoster.png" width="50%" />
	4. The data indicates 
		1. The 'Instructor First Name' is in Column D
		2. There are two different entries for 'Instructor First Name' for the specified ID.
			1. 9 entries of 'Jonah' and the first entry occurs on row 2
			2. 1 entry of 'Bartholomeow' which occurs on row 11
	5. From the data, it can be easily determined that the 'Bartholomeow' entry is likely incorrect.
	6. Switch to the Roster file window and make the appropriate correction
		1. In this case, the ID number on row 11 was not correct
		2. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/008-IDwrong.png" width="50%" />
	7. Return to the RVE window and it will indicate that the error appears to have been corrected
		1. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/008a-corrected.png" width="50%" />
8. Tap on the 'Errors' tab to select the next error
	1. Clear the 'RF' from Col B of the corrected error, or remove the entire row
	2. <img src="https://github.com/acornish123/NWEA_Roster_Validation_Error_Tool/blob/master/screenshots/009-NextError.png" width="80%" />
9. Return to the 'Dashboard' tab
	1. The error indicates 'May have been corrected by previous change'.  This is accurate since the ID number was corrected for the first error.


