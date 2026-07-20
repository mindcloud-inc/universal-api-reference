# List Model Versions with Clarifai

Retrieves model versions from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/models/:modelId/versions`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Model Versions](https://docs.clarifai.com/create/models/model-versions/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `modelId` | path | `string` | yes | Clarifai model ID. |
| `trained_only` | query | `boolean` | no | Return only trained versions. |
| `concept_ids` | query | `string` | no | Filter by concept IDs. |
