# Update Cell with Google Sheets

Updates a cell in a Google Sheets worksheet.

## Endpoint

- **Method:** `PUT`
- **Path:** `spreadsheets/:spreadsheetId/values/:worksheet!:cell`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Update Cell](https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets.values/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `worksheet` | path | `list<list>` | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. |
| `cell` | path | `string<string>` | yes | The cell you want to update, such as B3. |
| `values` | body | `string` | no | Send multiple values as a array. |
