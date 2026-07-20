# Get Model Labels with Matterport

Retrieves labels from a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Labels](https://static.matterport.com/api-doc/2024.07.44-main-g63d157b/reference/graphdoc/model/label.doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model labels. |
| `modelId` | body | `string` | yes | Matterport model ID. |
