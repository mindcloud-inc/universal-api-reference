# Create Row with Google Sheets

Creates a new row in a Google Sheets worksheet.

## Endpoint

- **Method:** `POST`
- **Path:** `spreadsheets/:spreadsheetId/values/:worksheet!:range:append`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Create Row](https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets.values/append)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `values` | body | `object<array>` | no | — |
| `worksheet` | path | `list<string>` | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. |
