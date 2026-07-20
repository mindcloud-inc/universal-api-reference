# Inpaint Image with ModelsLab

Creates an inpainted image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/realtime/inpaint`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Inpaint Image](https://docs.modelslab.com/image-generation/realtime-stable-diffusion/inpaint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Image URL to inpaint. |
| `mask_image` | body | `string` | no | Mask image URL for the inpainted region. |
| `prompt` | body | `string` | no | Prompt describing the masked-region fill. |
