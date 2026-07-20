# List Spreadsheet Columns with Google Sheets

Retrieves columns from a Google Sheets worksheet.

## Endpoint

- **Method:** `GET`
- **Path:** `spreadsheets/:spreadsheetId/values:method`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [List Spreadsheet Columns](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/batchGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `worksheet` | query | `list<string>` | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. |
| `columns` | query | `string<string>` | yes | Columns to fetch  - A - A1 |
| `end` | query | `number` | no | — |
| `start` | query | `number` | no | — |
