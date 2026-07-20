# Get Model Bundles with Matterport

Retrieves add-on bundles from a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Bundles](https://matterport.github.io/showcase-sdk/modelapi_ordering_addons.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model bundles. |
| `modelId` | body | `string` | yes | Matterport model ID. |
