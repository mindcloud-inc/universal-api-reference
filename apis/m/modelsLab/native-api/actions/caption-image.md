# Caption Image with ModelsLab

Creates an image caption in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/image_editing/caption`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Caption Image](https://docs.modelslab.com/image-editing/caption)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Image URL to caption. |
| `length` | body | `string` | no | Caption length: short, normal, or long. |
