# Create Try-On Generation with Glam AI

Creates a try-on generation in Glam AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/tryon`
- **Base URL:** `https://api.glam.ai/api/v1`
- **Official documentation:** [Create Try-On Generation](https://glam-ai.readme.io/reference/generate_tryon_tryon_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_url` | body | `string` | yes | URL of the person image for virtual try-on. |
| `garment_url` | body | `string` | yes | URL of the garment image to try on. |
| `mask_type` | body | `list` | yes | Clothing area to replace. Accepted values: `lower`, `overall`, `upper`. |
