# List Files with PixelBin.io

Retrieves files and folders from PixelBin.io storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/listFiles`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [List Files](https://www.pixelbin.io/docs/storage/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Find items with a matching format. |
| `name` | query | `string` | no | Find items with a matching name. |
| `onlyFiles` | query | `boolean` | no | If true, fetch only files. |
| `path` | query | `string` | no | Find items with a matching path. |
| `onlyFolders` | query | `boolean` | no | If true, fetch only folders. |
| `pageNo` | query | `number` | no | Page number. |
| `pageSize` | query | `number` | no | Page size. |
| `sort` | query | `string` | no | Key to sort results by. Use -suffix for descending order. |
