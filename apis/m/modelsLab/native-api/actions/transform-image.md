# Transform Image with ModelsLab

Creates a transformed image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/realtime/img2img`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Transform Image](https://docs.modelslab.com/image-generation/realtime-stable-diffusion/image-to-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Image URL to transform. |
| `prompt` | body | `string` | no | Prompt describing the desired transformation. |
