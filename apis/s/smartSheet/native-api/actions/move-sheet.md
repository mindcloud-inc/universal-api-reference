# Move Sheet with Smartsheet

Moves a sheet in Smartsheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/sheets/:sheetId/move`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Move Sheet](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/move-sheet)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `destinationId` | body | `number` | yes |
| `destinationType` | body | `string` | yes |
