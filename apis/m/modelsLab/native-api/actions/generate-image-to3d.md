# Generate Image To 3D with ModelsLab

Creates a 3D asset from an image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/3d/image_to_3d`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Generate Image To 3D](https://docs.modelslab.com/3d-api/image-to-3d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Source image URL for 3D generation. |
