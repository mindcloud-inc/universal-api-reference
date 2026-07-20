# Get Model Access with Matterport

Retrieves access details for a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Access](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/accessinfo.doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model access. |
| `modelId` | body | `string` | yes | Matterport model ID. |
| `pageSize` | body | `number` | no | Maximum number of access records to return. |
| `offset` | body | `string` | no | Pagination offset returned by the previous access response. |
