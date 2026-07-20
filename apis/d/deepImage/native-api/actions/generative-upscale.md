# Generative Upscale with DeepImage

Creates a generatively upscaled image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Generative Upscale](https://documentation.deep-image.ai/common-usecases/genarate-image-in-high-resolution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the image to upscale. |
| `width` | body | `number` | yes | Desired output width in pixels. |
| `height` | body | `number` | no | Optional output height in pixels when you want to force exact dimensions. |
