# Create Signed Multipart Upload URL with Erase.bg

Creates a signed multipart upload URL in Erase.bg.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v2.0/upload/signed-url`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Create Signed Multipart Upload URL](https://www.pixelbin.io/docs/api/upload-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expiry` | body | `number` | no | Expiry time in seconds for the presigned URL. |
| `format` | body | `string` | no | File format or extension. |
| `name` | body | `string` | no | Desired asset name. |
| `path` | body | `string` | no | Destination folder path. |
