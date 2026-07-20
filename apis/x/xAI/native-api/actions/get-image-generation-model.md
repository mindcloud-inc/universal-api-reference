# Get Image Generation Model with xAI

Retrieves an image generation model from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/image-generation-models/:model_id`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Get Image Generation Model](https://docs.x.ai/developers/rest-api-reference/inference/models#get-image-generation-model)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | path | `string` | no | ID of the image generation model to retrieve. |
