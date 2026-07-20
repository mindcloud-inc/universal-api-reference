# Get Model Image with Matterport

Retrieves image details for a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Image](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/photo.doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model photos. |
| `modelId` | body | `string` | yes | Matterport model ID. |
