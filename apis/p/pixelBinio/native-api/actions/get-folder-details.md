# Get Folder Details with PixelBin.io

Retrieves folder details from PixelBin.io storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/folders`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Get Folder Details](https://www.pixelbin.io/docs/storage/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Folder name to fetch. |
| `path` | query | `string` | no | Path containing the folder. Use an empty string for the root path. |
