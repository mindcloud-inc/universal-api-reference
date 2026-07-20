# Upload Asset From URL with Erase.bg

Creates a file in Erase.bg from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/upload/url`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Upload Asset From URL](https://www.pixelbin.io/docs/api/upload-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name to store the asset under. |
| `path` | body | `string` | no | Destination folder path. |
| `url` | body | `string` | yes | Public URL of the asset to import. |
