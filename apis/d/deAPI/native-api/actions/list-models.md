# List Models with deAPI

Retrieves available inference models from deAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/client/models`
- **Base URL:** `https://api.deapi.ai`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[inference_types]` | query | `string` | no | Comma-separated inference types such as txt2img,txt2audio,txt2video. |
| `page` | query | `string` | no | Page number for pagination. |
| `per_page` | query | `string` | no | Maximum number of models to return. |
