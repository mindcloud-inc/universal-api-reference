# List Models with Mistral AI

Retrieves available models from Mistral AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/models`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [List Models](https://docs.mistral.ai/api/endpoint/models#operation-list_models_v1_models_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `provider` | query | `string` | no | Optional model provider filter. |
| `model` | query | `string` | no | Optional model ID filter. |
