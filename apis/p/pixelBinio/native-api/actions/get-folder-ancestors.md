# Get Folder Ancestors with PixelBin.io

Retrieves folder ancestors from PixelBin.io storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/folders/:_id/ancestors`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Get Folder Ancestors](https://www.pixelbin.io/docs/storage/miscellaneous/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | path | `string` | yes | PixelBin folder _id returned by List Files or Get Folder Details. |
