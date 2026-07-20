# Get Row with Smartsheet

Retrieves a row from a Smartsheet sheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetId/rows/:rowId`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Get Row](https://developers.smartsheet.com/api/smartsheet/openapi/rows/get-row)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `rowId` | path | `number` | yes |
| `include` | query | `string` | no |
| `exclude` | query | `string` | no |
| `level` | query | `number` | no |
