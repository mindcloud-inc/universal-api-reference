# List Invokes with 88stacks Image Generator

Retrieves image generation requests for a model in 88stacks Image Generator.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/invokes`
- **Base URL:** `https://api.88stacks.com`
- **Official documentation:** [List Invokes](https://88stacks.com/docs/1.0/invokes/index.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | query | `string` | yes | Model ID whose invokes you want to list. |
