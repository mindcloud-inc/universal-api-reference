# Get Image Metadata with 1001fx

Retrieves metadata from an image file.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/getimagemeta`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Get Image Metadata](https://1001fx.com/functions/getimagemeta)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
