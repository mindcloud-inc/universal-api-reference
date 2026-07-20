# List Models with Airiam AI

Retrieves a list of models from Airiam AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/models`
- **Base URL:** `https://platform.sectorflow.ai`
- **Official documentation:** [List Models](https://docs.ai.airiam.com/reference/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeSystem` | query | `boolean` | no | Whether to include system models. |
| `modelRating` | query | `number` | no | Filter models by rating. |
