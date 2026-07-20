# Update File with Erase.bg

Updates a file in Erase.bg storage.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/service/platform/assets/v1.0/files/:fileId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Update File](https://www.pixelbin.io/docs/storage/rename-file/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | Combination of path and name of the file. |
| `isActive` | body | `boolean` | no | Whether the file should remain active. |
| `name` | body | `string` | no | Updated file name. |
| `path` | body | `string` | no | Updated folder path. |
