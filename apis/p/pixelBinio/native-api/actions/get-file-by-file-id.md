# Get File By File ID with PixelBin.io

Retrieves a file from PixelBin.io by file ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/files/:fileId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Get File By File ID](https://www.pixelbin.io/docs/storage/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | Combined PixelBin file path and file name. |
