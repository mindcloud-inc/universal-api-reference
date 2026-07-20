# Get Sheet Summary with Smartsheet

Retrieves a sheet summary from Smartsheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetId/summary`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Get Sheet Summary](https://developers.smartsheet.com/api/smartsheet/openapi/sheetsummary/sheetsummary)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `include` | query | `string` | no |
| `exclude` | query | `string` | no |
