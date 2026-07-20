# Serve CDN Image with VisionFly

Retrieves an image from the VisionFly CDN.

## Endpoint

- **Method:** `GET`
- **Path:** `/cdn/:image_id`
- **Base URL:** `https://api.visionfly.ai`
- **Official documentation:** [Serve CDN Image](https://api.visionfly.ai/docs#/default/serve_image_cdn__image_id__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `f` | query | `string` | no | Output format such as webp, avif, png, jpeg, or auto. |
| `h` | query | `string` | no | Optional output height in pixels. |
| `image_id` | path | `string` | no | VisionFly image identifier. |
| `opt` | query | `string` | no | Apply smart optimization. |
| `q` | query | `string` | no | Output quality from 1 to 100. |
| `w` | query | `string` | no | Optional output width in pixels. |
