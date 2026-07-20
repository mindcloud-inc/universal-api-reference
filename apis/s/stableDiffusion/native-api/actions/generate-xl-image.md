# Generate XL Image with Stable Diffusion

Generates an XL image in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/generation/stable-diffusion-xl-1024-v1-0/text-to-image`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate XL Image](https://staging-api.stability.ai/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text_prompts[0][text]` | body | `string` | yes | Primary text prompt for image generation. |
