# Denoise Image with DeepImage

Creates a denoised image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Denoise Image](https://documentation.deep-image.ai/image-processing/denoise-and-sharpen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to denoise. |
| `denoise_parameters.type` | body | `string` | no | Optional denoise model version. Use v1 or v2. |
