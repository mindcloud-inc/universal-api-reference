# Get Model Measurement Paths with Matterport

Retrieves measurement paths from a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Measurement Paths](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/measurementpath.doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for measurement paths. |
| `modelId` | body | `string` | yes | Matterport model ID. |
