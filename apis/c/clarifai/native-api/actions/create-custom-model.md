# Create Custom Model with Clarifai

Creates a custom model in Clarifai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/me/apps/:appId/models`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Create Custom Model](https://docs.clarifai.com/create/models/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `model` | body | `object` | yes | Model to create. |
| `id` | body | `string` | yes | Model ID. |
| `model_type_id` | body | `string` | yes | Clarifai model type ID. |
