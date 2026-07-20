# Process Image and Return Result with DeepImage

Processes an image and returns the result from DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Process Image and Return Result](https://documentation.deep-image.ai/api-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to process. |
| `preset` | body | `string` | no | Optional DeepImage preset name, such as ecommerce or real_estate. |
| `output_format` | body | `string` | no | Optional output image format: jpg, jpeg, png, or webp. |
| `quality` | body | `number` | no | Optional output quality from 0 to 100. |
