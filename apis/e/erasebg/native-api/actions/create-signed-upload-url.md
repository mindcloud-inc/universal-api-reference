# Create Signed Upload URL with Erase.bg

Creates a signed upload URL in Erase.bg.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/upload/signed-url`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Create Signed Upload URL](https://www.pixelbin.io/docs/api/upload-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | no | File format or extension. |
| `name` | body | `string` | no | Desired asset name. |
| `path` | body | `string` | no | Destination folder path. |
