# Update Column with Smartsheet

Updates an existing column in a Smartsheet sheet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sheets/:sheetId/columns/:columnId`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Update Column](https://developers.smartsheet.com/api/smartsheet/openapi/columns/update-column)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `columnId` | path | `number` | yes |
| `title` | body | `string` | no |
| `type` | body | `string` | no |
| `options[]` | body | `array<string>` | no |
| `description` | body | `string` | no |
