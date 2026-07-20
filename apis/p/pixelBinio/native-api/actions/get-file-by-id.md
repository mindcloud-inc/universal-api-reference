# Get File By ID with PixelBin.io

Retrieves a file from PixelBin.io by internal ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/files/id/:_id`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Get File By ID](https://www.pixelbin.io/docs/storage/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | path | `string` | yes | PixelBin file _id returned by List Files. |
