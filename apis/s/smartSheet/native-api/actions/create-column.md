# Create Column with Smartsheet

Creates a new column in a Smartsheet sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/sheets/:sheetId/columns`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Create Column](https://developers.smartsheet.com/api/smartsheet/openapi/columns/add-column)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `index` | body | `number` | yes |
| `title` | body | `string` | yes |
| `type` | body | `string` | yes |
| `options[]` | body | `array<string>` | no |
| `description` | body | `string` | no |
