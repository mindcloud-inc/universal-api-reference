# Get Model with Airiam AI

Retrieves a model from Airiam AI by model ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/models/:baseModel`
- **Base URL:** `https://platform.sectorflow.ai`
- **Official documentation:** [Get Model](https://docs.ai.airiam.com/reference/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseModel` | path | `string` | yes | Model base identifier from the baseModel field, such as inflection-3-pi. |
