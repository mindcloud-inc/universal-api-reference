# Search Models with Clarifai

Finds models in Clarifai by model ID or name.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/me/apps/:appId/models/searches`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Search Models](https://docs.clarifai.com/create/models/manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `model_query` | body | `object` | yes | Model search query. |
| `model_query.name` | body | `string` | yes | Model ID or name to search for. |
| `model_query.model_type_id` | body | `string` | no | Filter search by model type ID. |
