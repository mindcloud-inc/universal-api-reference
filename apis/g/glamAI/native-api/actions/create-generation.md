# Create Generation with Glam AI

Creates an image generation in Glam AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/generate`
- **Base URL:** `https://api.glam.ai/api/v1`
- **Official documentation:** [Create Generation](https://glam-ai.readme.io/reference/generate_generate_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_url` | body | `string` | yes | URL of the image or video to transform. |
| `filter_name` | body | `string` | yes | Glam AI filter name, such as beetlejuice. |
