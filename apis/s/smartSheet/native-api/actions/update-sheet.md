# Update Sheet with Smartsheet

Updates an existing sheet in Smartsheet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sheets/:sheetId`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Update Sheet](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/update-sheet)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `name` | body | `string` | no |
| `projectSettings` | body | `object` | no |
| `userSettings` | body | `object` | no |
