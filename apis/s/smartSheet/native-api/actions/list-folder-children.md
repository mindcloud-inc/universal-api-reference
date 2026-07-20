# List Folder Children with Smartsheet

Retrieves items in a Smartsheet folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folderId/children`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [List Folder Children](https://developers.smartsheet.com/api/smartsheet/openapi/folders/list-folder-children)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderId` | path | `number` | yes |
| `childrenResourceTypes` | query | `string` | no |
| `include` | query | `string` | no |
| `numericDates` | query | `boolean` | no |
| `maxItems` | query | `number` | no |
| `lastKey` | query | `string` | no |
