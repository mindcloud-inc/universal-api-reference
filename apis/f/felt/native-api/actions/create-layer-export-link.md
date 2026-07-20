# Create Layer Export Link with Felt

Retrieves a layer export link from Felt.

## Endpoint

- **Method:** `GET`
- **Path:** `/maps/:mapId/layers/:layerId/get_export_link`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Create Layer Export Link](https://developers.felt.com/rest-api/api-reference/layers/layer-exports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map where the layer is located. |
| `layerId` | path | `string` | yes | The ID of the layer to export. |
