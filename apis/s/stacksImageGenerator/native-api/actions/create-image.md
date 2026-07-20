# Create Image with 88stacks Image Generator

Creates images in 88stacks Image Generator from a prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/invokes`
- **Base URL:** `https://api.88stacks.com`
- **Official documentation:** [Create Image](https://88stacks.com/docs/1.0/invokes/create.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt text to generate images from. |
| `model_id` | body | `string` | no | Model ID to generate images with. |
| `num_images` | body | `number` | no | Number of images to create per prompt. Default 4, max 8. |
| `image_url` | body | `string` | no | Public image URL to use as the source image. |
| `callback` | body | `string` | no | Webhook URL to call when image generation completes. |
| `key` | body | `string` | no | Optional key used for easier content lookups. |
