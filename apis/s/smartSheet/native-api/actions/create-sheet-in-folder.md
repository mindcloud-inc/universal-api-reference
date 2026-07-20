# Create Sheet in Folder with Smartsheet

Creates a new sheet in a Smartsheet folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folderId/sheets`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Create Sheet in Folder](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/create-sheet-in-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `columns[]` | body | `array<object>` | no |
| `fromId` | body | `number` | no |
| `include` | query | `string` | no |
