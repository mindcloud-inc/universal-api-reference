# List Spreadsheet Worksheets with Google Sheets

Retrieves worksheets from a Google Sheets spreadsheet.

## Endpoint

- **Method:** `GET`
- **Path:** `spreadsheets/:spreadsheetId?fields=sheets.properties`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [List Spreadsheet Worksheets](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `string<string>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
