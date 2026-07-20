# Update Spreadsheet Row with Google Sheets

Updates a row in a Google Sheets worksheet.

## Endpoint

- **Method:** `PUT`
- **Path:** `spreadsheets/:spreadsheetId/values/:worksheet!:row::row`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Update Spreadsheet Row](https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets.values/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `values` | body | `object<string>` | no | — |
| `worksheet` | path | `list<list>` | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. |
| `row` | path | `string<string>` | no | The row number to update. Note: row 1 typically contains the spreadsheet headers, so you may want to avoid modifying it. |
