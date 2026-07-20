# Publish Map Layer Group with Felt

Publishes a map layer group to Felt's library.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/layer_groups/:layerGroupId/publish`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Publish Map Layer Group](https://developers.felt.com/rest-api/api-reference/layers/layer-library)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map where the layer group is located. |
| `layerGroupId` | path | `string` | yes | The ID of the layer group to publish. |
| `name` | body | `string` | no | The name to publish the layer group under. |
