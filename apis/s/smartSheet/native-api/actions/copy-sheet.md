# Copy Sheet with Smartsheet

Creates a copy of a sheet in Smartsheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/sheets/:sheetId/copy`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Copy Sheet](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/copy-sheet)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `destinationId` | body | `number` | yes |
| `destinationType` | body | `string` | no |
| `newName` | body | `string` | no |
