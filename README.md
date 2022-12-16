# NWEA Roster Format Checker
Spreadsheet tool which identifies most common roster (csv) errors encountered during the initial file checks

## About
Spreadsheet tool which can quickly identify common errors which can cause the roster file (.csv) to fail during the initial file check.  It purely uses advanced spreadsheet functions in order to avoid security concerns and installation issues.

<img src="https://github.com/acornish123/Roster_FormatChecker/blob/master/screenshots/failScreen.png" width="50%" />

## Getting Started
Simply download the spreadsheet, open in MS Excel, then follow the instructions.

## Usage
1. Prior to using the tool, create a backup copy of your roster file.
2. Place your roster file in the same directory/folder as the Roster Format Checker (RFC) spreadsheet tool.  Both of the spreadsheets must remain open at the same time.
3. Open both the RFC and the roster file.
4. STEP 1 - Enter the filename of your roster file WITHOUT the extension.  The tool will only link to a 'csv' file.
	1. After entering the name, press enter or click outside the cell. The yellow border will change to green if it successfully links to the roster file.
	3. <img src="https://github.com/acornish123/Roster_FormatChecker/blob/master/screenshots/filename.png" width="25%" />
5. STEP 2 - Correct any header (Row 1) errors indicated
	1. Corrections made in your roster file should automatically update the tool.  It may be necessary to click outside of the cell or press F9 in the tool to refresh the data.
	1. You can copy from the "Missing Headers" section and paste to your roster if needed.
	2. All headers must be present, must match exactly and ARE case sensitive.
	3. It is advisable to keep the same order of headers as the template, though it is not required.
	4. If there are not any remaining errors listed, but the 'Amt of headers' is greater than 29 then are additional header entries in your roster file. Remove any extra header entries past Column AC in row 1.
6. STEP 3 - Remove extraneous entries
	1. The tool checks the most common areas that accidental entries may occur.
	2. To ensure there are not any accidental entries outside of the checked area, follow the steps indicated in the tool.
7. STEP 4 - Save roster
	1. It is essential that the roster file is saved in the correct CSV format.
8. Import roster again.