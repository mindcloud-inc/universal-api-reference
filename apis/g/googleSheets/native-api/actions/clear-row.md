# Clear Row with Google Sheets

Clears row contents in Google Sheets while keeping rows intact.

## Endpoint

- **Method:** `POST`
- **Path:** `spreadsheets/:spreadsheetId/values:method`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Clear Row](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/batchClear)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `worksheet` | query | `list<string>` | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. |
| `rows` | body | `string` | yes | Rows remain intact, only their contents will be cleared. Accepts:  - Individual row numbers (e.g. 3) - Ranges (e.g. 3–5) - Comma-separated lists (e.g. 3, 4, 6) |
