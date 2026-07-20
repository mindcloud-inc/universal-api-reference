# Get Image Generation Model with Grok

Retrieves a specific image generation model from Grok.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/image-generation-models/:model_id`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Get Image Generation Model](https://docs.x.ai/developers/rest-api-reference/inference/models#get-image-generation-model)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | path | `string` | yes | Image generation model identifier. |
