# List Sheet Worksheets with GMass

Retrieves worksheets from a connected Google Sheet in GMass.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetid/worksheets`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [List Sheet Worksheets](https://api.gmass.co/docs#tag/Sheets/operation/Sheets_WorksheetList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sheetid` | path | `string` | yes | Google Sheet ID to list worksheets for. |
