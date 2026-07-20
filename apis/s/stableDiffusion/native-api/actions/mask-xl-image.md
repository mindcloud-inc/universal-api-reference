# Mask XL Image with Stable Diffusion

Masks an XL image in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/generation/stable-diffusion-xl-1024-v1-0/image-to-image/masking`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Mask XL Image](https://staging-api.stability.ai/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | yes | Source image to transform. |
| `mask_source` | body | `string` | yes | Masking strategy to use for the source image. |
| `text_prompts[0][text]` | body | `string` | yes | Primary text prompt for the masked image generation. |
