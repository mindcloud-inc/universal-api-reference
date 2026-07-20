# Get Model Geo Coordinates with Matterport

Retrieves geo coordinates for a Matterport model.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [Get Model Geo Coordinates](https://matterport.github.io/showcase-sdk/modelapi_geocoordinates.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | GraphQL query for model geo coordinates. |
| `modelId` | body | `string` | yes | Matterport model ID. |
