# Create Signed URL with PixelBin.io

Creates a new signed upload URL in PixelBin.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/upload/signed-url`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Create Signed URL](https://www.pixelbin.io/docs/api/upload-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `access` | body | `string` | yes |
| `format` | body | `string` | yes |
| `name` | body | `string` | yes |
| `path` | body | `string` | yes |
