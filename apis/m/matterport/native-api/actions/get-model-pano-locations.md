# Get Model Pano Locations with Matterport

Retrieves panoramic image locations from a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Pano Locations](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/panoramicimagelocation.doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model pano locations. |
| `modelId` | body | `string` | yes | Matterport model ID. |
