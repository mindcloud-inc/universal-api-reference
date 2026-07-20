# Upscale Anime Image with DeepAI

Creates a denoised, upscaled image in DeepAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/waifu2x`
- **Base URL:** `https://api.deepai.org/api`
- **Official documentation:** [Upscale Anime Image](https://api.deepai.org/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | The image URL or uploaded file to upscale with anime-focused processing. |
