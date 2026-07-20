# Upscale Image with Picsart

Creates an upscaled image in Picsart.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/1.0/upscale`
- **Base URL:** `https://api.picsart.io`
- **Official documentation:** [Upscale Image](https://docs.picsart.io/reference/image-upscale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL. |
| `upscale_factor` | body | `number` | yes | Choose one of the supported upscale factors. |
| `format` | body | `string` | no | Optional output image format. |
