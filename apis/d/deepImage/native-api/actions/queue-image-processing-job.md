# Queue Image Processing Job with DeepImage

Queues an image processing job in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Queue Image Processing Job](https://documentation.deep-image.ai/api-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to queue for processing. |
| `preset` | body | `string` | no | Optional DeepImage preset name, such as ecommerce or real_estate. |
| `output_format` | body | `string` | no | Optional output image format: jpg, jpeg, png, or webp. |
| `quality` | body | `number` | no | Optional output quality from 0 to 100. |
