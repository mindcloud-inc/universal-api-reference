# Get Model Rooms with Matterport

Retrieves rooms from a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Rooms](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/modelroom.doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model rooms. |
| `modelId` | body | `string` | yes | Matterport model ID. |
