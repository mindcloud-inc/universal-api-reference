# Upscale by Percentage with DeepImage

Creates an upscaled image by percentage in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Upscale by Percentage](https://documentation.deep-image.ai/image-processing/resize-and-padding)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to upscale. |
| `width` | body | `string` | yes | Upscale percentage string such as 200% or 400%. |
