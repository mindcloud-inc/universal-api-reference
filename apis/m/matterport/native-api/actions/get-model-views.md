# Get Model Views with Matterport

Retrieves saved views from a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Views](https://matterport.github.io/showcase-sdk/modelapi_views_and_layers.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model views. |
| `modelId` | body | `string` | yes | Matterport model ID. |
