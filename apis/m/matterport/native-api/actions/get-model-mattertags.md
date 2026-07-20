# Get Model Mattertags with Matterport

Retrieves Mattertags from a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Mattertags](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/mattertag.doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model Mattertags. |
| `modelId` | body | `string` | yes | Matterport model ID. |
