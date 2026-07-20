# Update Folder with PixelBin.io

Updates an existing folder in PixelBin.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/service/platform/assets/v1.0/folders/:folderId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Update Folder](https://www.pixelbin.io/docs/storage/miscellaneous/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderId` | path | `string` | yes |
| `isActive` | body | `boolean` | yes |
