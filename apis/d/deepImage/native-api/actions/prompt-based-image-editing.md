# Prompt-Based Image Editing with DeepImage

Creates an edited image from a prompt in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Prompt-Based Image Editing](https://documentation.deep-image.ai/image-processing/prompt-based-image-editing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `background.generate.description` | body | `string` | yes | Text prompt describing the edit you want to apply. |
| `background.generate.context_images[0]` | body | `string` | yes | Public URL of the source image used as context for the edit. |
| `width` | body | `number` | no | Target width of the output image. |
| `height` | body | `number` | no | Target height of the output image. |
