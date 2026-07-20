# Create Worksheet with Google Sheets

Creates a new worksheet in Google Sheets.

## Endpoint

- **Method:** `POST`
- **Path:** `spreadsheets/:spreadsheetId:batchUpdate`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Create Worksheet](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | — |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
