# Update Folder with Erase.bg

Updates a folder in Erase.bg storage.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/service/platform/assets/v1.0/folders/:folderId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Update Folder](https://www.pixelbin.io/docs/storage/miscellaneous/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder identifier composed from path and name. |
| `isActive` | body | `boolean` | no | Whether the folder should remain active. |
