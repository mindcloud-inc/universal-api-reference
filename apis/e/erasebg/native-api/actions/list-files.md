# List Files with Erase.bg

Retrieves files from Erase.bg storage by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/listFiles`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [List Files](https://www.pixelbin.io/docs/storage/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Filter by file format. |
| `name` | query | `string` | no | Find items with a matching name. |
| `onlyFiles` | query | `boolean` | no | Fixed Stage 1 test-action query flag for PixelBin listFiles. |
| `path` | query | `string` | no | Find items in the specified path. |
| `onlyFolders` | query | `boolean` | no | Fixed Stage 1 test-action query flag for PixelBin listFiles. |
| `pageNo` | query | `number` | no | Fixed Stage 1 page number for the Erase.bg connection test action. |
| `pageSize` | query | `number` | no | Fixed Stage 1 page size for the Erase.bg connection test action. |
| `sort` | query | `string` | no | Fixed Stage 1 sort field for the Erase.bg connection test action. |
