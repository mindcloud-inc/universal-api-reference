# Remove Object From Image with ModelsLab

Creates an object-removed image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/image_editing/object_remover`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Remove Object From Image](https://docs.modelslab.com/image-editing/object-remover)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Image URL for object removal. |
| `object_prompt` | body | `string` | no | Object or region to remove from the image. |
