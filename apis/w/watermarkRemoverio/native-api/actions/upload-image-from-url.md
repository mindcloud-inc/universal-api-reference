# Upload Image From URL with WatermarkRemover.io

Uploads an image to WatermarkRemover.io from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pixelbin.io/service/platform/assets/v1.0/upload/url`
- **Base URL:** `https://cdn.pixelbin.io`
- **Official documentation:** [Upload Image From URL](https://www.pixelbin.io/docs/api/upload-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filenameOverride` | body | `string` | no | Whether PixelBin should append/override the filename when a duplicate exists. |
| `name` | body | `string` | no | Optional asset name for the uploaded image. |
| `path` | body | `string` | no | Optional destination folder path in PixelBin storage. |
| `url` | body | `string` | no | Public URL of the asset to upload into PixelBin storage. |
