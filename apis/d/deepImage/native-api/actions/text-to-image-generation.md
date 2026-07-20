# Text-to-Image Generation with DeepImage

Creates an image from text in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Text-to-Image Generation](https://documentation.deep-image.ai/image-processing/image-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `background.generate.description` | body | `string` | yes | Prompt describing the image to generate. |
| `width` | body | `number` | no | Target width of the generated image. |
| `height` | body | `number` | no | Target height of the generated image. |
