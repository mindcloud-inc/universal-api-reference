# Get Map Layer Group with Felt

Retrieves a map layer group from Felt.

## Endpoint

- **Method:** `GET`
- **Path:** `/maps/:mapId/layer_groups/:layerGroupId`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Get Map Layer Group](https://developers.felt.com/rest-api/api-reference/layers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map. |
| `layerGroupId` | path | `string` | yes | The ID of the layer group. |
