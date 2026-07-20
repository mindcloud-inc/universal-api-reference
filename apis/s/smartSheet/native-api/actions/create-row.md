# Create Row with Smartsheet

Creates a new row in a Smartsheet sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/sheets/:sheetId/rows`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Create Row](https://developers.smartsheet.com/api/smartsheet/openapi/rows/add-rows)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `above` | body | `string` | no |
| `sheetId` | path | `number` | yes |
| `toTop` | body | `boolean` | no |
| `toBottom` | body | `boolean` | no |
| `parentId` | body | `number` | no |
| `siblingId` | body | `number` | no |
