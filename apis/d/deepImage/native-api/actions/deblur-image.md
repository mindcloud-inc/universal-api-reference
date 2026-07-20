# Deblur Image with DeepImage

Creates a deblurred image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Deblur Image](https://documentation.deep-image.ai/image-processing/denoise-and-sharpen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to deblur. |
| `deblur_parameters.type` | body | `string` | no | Optional deblur model version. Use v1 or v2. |
