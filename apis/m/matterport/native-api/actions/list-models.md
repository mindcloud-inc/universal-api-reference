# List Models with Matterport

Retrieves models from your Matterport account.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [List Models](https://matterport.github.io/showcase-sdk/modelapi_models_ref.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Hidden GraphQL query for listing models. |
| `modelQuery` | body | `string` | no | Matterport model search query. Use * for all active models. |
| `pageSize` | body | `number` | no | Maximum number of models to return. |
| `offset` | body | `string` | no | Next page offset returned by a previous models query. |
