# Get Model Uploaders with Matterport

Retrieves uploader details for a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Uploaders](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/usermetadata.doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model uploaders. |
| `modelId` | body | `string` | yes | Matterport model ID. |
