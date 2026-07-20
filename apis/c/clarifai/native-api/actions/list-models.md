# List Models with Clarifai

Retrieves models from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/models`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Models](https://docs.clarifai.com/create/models/manage/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `search` | query | `string` | no | Search term for model ID or name. |
| `model_type_id` | query | `string` | no | Filter by model type ID. |
| `trained_only` | query | `boolean` | no | Return only trained models. |
