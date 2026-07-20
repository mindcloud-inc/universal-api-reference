# Generate Flux Image with ModelsLab

Creates a Flux image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/images/text2img`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Generate Flux Image](https://docs.modelslab.com/image-generation/flux/flux-text-to-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | body | `string` | no | Model identifier, for example flux. |
| `prompt` | body | `string` | no | Text prompt describing the Flux image to generate. |
