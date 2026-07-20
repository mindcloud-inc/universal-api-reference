# Upload Asset with 1001fx

Uploads an asset to 1001fx and returns a temporary download URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/uploadasset`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Upload Asset](https://1001fx.com/functions/uploadasset)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
