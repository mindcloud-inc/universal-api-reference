# Create Dataset with Clarifai

Creates a new dataset in Clarifai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/me/apps/:appId/datasets`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Create Dataset](https://docs.clarifai.com/create/datasets/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `datasets[]` | body | `array<object>` | yes | Datasets to create. |
| `datasets[].id` | body | `string` | yes | Dataset ID. |
| `datasets[].description` | body | `string` | no | Dataset description. |
