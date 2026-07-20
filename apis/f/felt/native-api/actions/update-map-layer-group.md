# Update Map Layer Group with Felt

Updates an existing map layer group in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/layer_groups/:layerGroupId`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Update Map Layer Group](https://developers.felt.com/rest-api/api-reference/layers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map. |
| `layerGroupId` | path | `string` | yes | The ID of the layer group. |
| `name` | body | `string` | yes | Updated layer group name. |
| `caption` | body | `string` | no | Updated layer group caption. |
| `legend_visibility` | body | `list` | no | Controls whether the layer group appears in the legend. Accepted values: `0`, `1`. |
| `visibility_interaction` | body | `list` | no | Controls how the layer group appears in the legend. Accepted values: `0`, `1`. |
