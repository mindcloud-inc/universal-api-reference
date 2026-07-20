# Get File By File ID with Erase.bg

Retrieves a file from Erase.bg by file ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/files/:fileId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Get File By File ID](https://www.pixelbin.io/docs/storage/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | Combination of path and name of the file. |
