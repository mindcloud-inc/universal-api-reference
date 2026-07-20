# Check Custom Export Status with Felt

Retrieves custom layer export status from Felt.

## Endpoint

- **Method:** `GET`
- **Path:** `/maps/:mapId/layers/:layerId/custom_exports/:exportId`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Check Custom Export Status](https://developers.felt.com/rest-api/api-reference/layers/layer-exports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map where the layer is located. |
| `layerId` | path | `string` | yes | The ID of the layer to export. |
| `exportId` | path | `string` | yes | The ID of the custom export request. |
