# Upload Image to CDN with VisionFly

Uploads an image to the VisionFly CDN.

## Endpoint

- **Method:** `POST`
- **Path:** `/cdn/upload`
- **Base URL:** `https://api.visionfly.ai`
- **Official documentation:** [Upload Image to CDN](https://api.visionfly.ai/docs#/default/upload_image_cdn_upload_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | Local file path or file input to upload to VisionFly. |
| `project` | query | `string` | no | Optional project slug to organize the uploaded image. |
