# Publish Map Layer with Felt

Publishes a map layer to Felt's library.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/layers/:layerId/publish`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Publish Map Layer](https://developers.felt.com/rest-api/api-reference/layers/layer-library)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map where the layer is located. |
| `layerId` | path | `string` | yes | The ID of the layer to publish. |
| `name` | body | `string` | no | The name to publish the layer under. |
