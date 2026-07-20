# List Model Concepts with Clarifai

Retrieves model concepts from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/models/:modelId/concepts`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Model Concepts](https://docs.clarifai.com/create/models/manage/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `modelId` | path | `string` | yes | Clarifai model ID. |
| `version_id` | query | `string` | no | Specific model version ID. |
| `search` | query | `string` | no | Search term for model concepts. |
