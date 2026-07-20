# Generate Text To 3D with ModelsLab

Creates a 3D asset from text in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/3d/text_to_3d`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Generate Text To 3D](https://docs.modelslab.com/3d-api/text-to-3d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | no | Prompt describing the 3D asset to generate. |
