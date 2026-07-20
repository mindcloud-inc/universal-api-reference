# List Generated Assets with ModelsLab

Retrieves generated assets from ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/assets_generated`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [List Generated Assets](https://docs.modelslab.com/general-api/assets-generated)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | body | `string` | no | Page number for generated assets. |
| `per_page` | body | `string` | no | Number of assets to return per page, up to 30. |
| `type` | body | `string` | no | Generated asset type to list: image, video, voice, or 3d. |
