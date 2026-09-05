# Append Rows with Google Sheets

Appends rows to a Google Sheets worksheet.

## Endpoint

- **Method:** `POST`
- **Path:** `spreadsheets/:spreadsheetId/values/:worksheet!:range:append`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Append Rows](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/append)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `worksheet` | path | `list<list>` | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. |
| `values[]` | body | `array<object>` | yes | Rows to append to the worksheet. Map an array of row objects from a previous step, then map each column field below (Col 1, Col 2, etc.) from the current row. The action still accepts Google Sheets' native 2D array format when supplied directly. |
| `values[].col1` | body | `string` | no | First cell value for each appended row. |
| `values[].col2` | body | `string` | no | Second cell value for each appended row. |
| `values[].col3` | body | `string` | no | Third cell value for each appended row. |
| `values[].col4` | body | `string` | no | Fourth cell value for each appended row. |
| `values[].col5` | body | `string` | no | Fifth cell value for each appended row. |
