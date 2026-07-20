# Delete Row with Google Sheets

Deletes a row from a Google Sheets worksheet.

## Endpoint

- **Method:** `POST`
- **Path:** `spreadsheets/:spreadsheetId:method`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Delete Row](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `worksheet` | body | `list<string>` | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. |
| `row` | body | `string` | yes | — |
