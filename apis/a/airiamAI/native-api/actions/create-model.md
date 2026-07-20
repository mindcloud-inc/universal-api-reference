# Create Model with Airiam AI

Creates a new model in Airiam AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/models`
- **Base URL:** `https://platform.sectorflow.ai`
- **Official documentation:** [Create Model](https://docs.ai.airiam.com/reference/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Model display name. |
| `baseModel` | body | `string` | no | Provider base model identifier. |
| `url` | body | `string` | yes | Model endpoint URL. |
| `modelApiKey` | body | `string` | yes | API key for the model endpoint. |
