# Generate Realtime Image with ModelsLab

Creates a realtime image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/realtime/text2img`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Generate Realtime Image](https://docs.modelslab.com/image-generation/realtime-stable-diffusion/text-to-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | no | Text prompt describing the image to generate. |
