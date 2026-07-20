# Remove Image Background with ModelsLab

Creates a background-removed image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/image_editing/removebg_createmask`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Remove Image Background](https://docs.modelslab.com/image-editing/removebg-createmask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Image URL for background removal. |
