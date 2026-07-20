# Batch Update Spreadsheet Values with Google Sheets

Updates explicit A1 ranges in Google Sheets.

## Endpoint

- **Method:** `POST`
- **Path:** `spreadsheets/:spreadsheetId/:batchUpdate`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Batch Update Spreadsheet Values](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `data[]` | body | `array` | no | An array of range/value objects to update in a single request. |
