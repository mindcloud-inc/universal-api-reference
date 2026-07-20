# Upscale Image with ModelsLab

Creates an upscaled image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/image_editing/super_resolution`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Upscale Image](https://docs.modelslab.com/image-editing/super-resolution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Image URL to upscale. |
| `scale` | body | `string` | no | Upscale factor, usually 2. |
