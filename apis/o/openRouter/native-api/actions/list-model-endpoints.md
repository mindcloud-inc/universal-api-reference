# List Model Endpoints with OpenRouter

Retrieves endpoints for a specific model in OpenRouter.

## Endpoint

- **Method:** `GET`
- **Path:** `/models/:author/:slug/endpoints`
- **Base URL:** `https://openrouter.ai/api/v1/`
- **Official documentation:** [List Model Endpoints](https://openrouter.ai/docs/api/api-reference/endpoints/list-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author` | path | `string` | yes | Model author segment used in the path. |
| `slug` | path | `string` | yes | Model slug segment used in the path. |
