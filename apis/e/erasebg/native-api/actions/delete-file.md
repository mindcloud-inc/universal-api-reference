# Delete File with Erase.bg

Deletes a file from Erase.bg storage.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/service/platform/assets/v1.0/files/:fileId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Delete File](https://www.pixelbin.io/docs/storage/delete-files/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | Combination of path and name of the file. |
