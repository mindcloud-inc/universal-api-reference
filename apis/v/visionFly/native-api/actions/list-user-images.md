# List User Images with VisionFly

Retrieves user images from the VisionFly CDN.

## Endpoint

- **Method:** `GET`
- **Path:** `/cdn/images`
- **Base URL:** `https://api.visionfly.ai`
- **Official documentation:** [List User Images](https://api.visionfly.ai/docs#/default/list_images_cdn_images_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Pagination cursor from a previous response. |
| `limit` | query | `string` | no | Maximum number of images to return. |
| `project` | query | `string` | no | Optional project slug filter. |
