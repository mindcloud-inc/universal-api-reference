# Get Spreadsheet Metadata with Google Sheets

Retrieves spreadsheet metadata from Google Sheets.

## Endpoint

- **Method:** `GET`
- **Path:** `spreadsheets/:spreadsheetId`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [Get Spreadsheet Metadata](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spreadsheetId` | path | `list<list>` | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. |
| `ranges` | query | `string` | no | — |
| `includeGridData` | query | `boolean` | no | — |
