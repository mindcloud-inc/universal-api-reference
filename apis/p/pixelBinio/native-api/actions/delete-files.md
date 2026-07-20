# Delete Files with PixelBin.io

Deletes multiple files from PixelBin.io storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/files/delete`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Delete Files](https://www.pixelbin.io/docs/storage/miscellaneous/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Array of file record IDs to delete. |
