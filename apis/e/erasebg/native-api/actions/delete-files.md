# Delete Files with Erase.bg

Deletes multiple files from Erase.bg storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/files/delete`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Delete Files](https://www.pixelbin.io/docs/storage/delete-files/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Array of file _ids to delete. |
