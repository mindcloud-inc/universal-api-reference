# Delete File with PixelBin.io

Deletes an existing file from PixelBin.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/service/platform/assets/v1.0/files/:fileId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Delete File](https://www.pixelbin.io/docs/storage/miscellaneous/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | Combined file path and file name for the file to delete. |
