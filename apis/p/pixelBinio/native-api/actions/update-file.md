# Update File with PixelBin.io

Updates an existing file in PixelBin.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/service/platform/assets/v1.0/files/:fileId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Update File](https://www.pixelbin.io/docs/storage/miscellaneous/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access` | body | `string` | no | Updated asset access level. |
| `fileId` | path | `string` | yes | Combined file path and file name for the file to update. |
| `isActive` | body | `boolean` | no | Whether the file remains active. |
| `metadata` | body | `object` | no | Updated metadata object for the file. |
| `name` | body | `string` | no | Updated file name. |
| `path` | body | `string` | no | Updated folder path. |
| `tags[]` | body | `array<string>` | no | Updated tags for the file. |
