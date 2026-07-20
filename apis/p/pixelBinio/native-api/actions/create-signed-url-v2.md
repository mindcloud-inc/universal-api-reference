# Create Signed URL V2 with PixelBin.io

Creates a new signed multipart upload URL in PixelBin.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v2.0/upload/signed-url`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Create Signed URL V2](https://www.pixelbin.io/docs/api/upload-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `access` | body | `string` | yes |
| `expiry` | body | `number` | yes |
| `format` | body | `string` | yes |
| `name` | body | `string` | yes |
| `path` | body | `string` | yes |
