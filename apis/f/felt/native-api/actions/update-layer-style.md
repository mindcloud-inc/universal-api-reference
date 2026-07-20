# Update Layer Style with Felt

Updates a map layer style in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/layers/:layerId/update_style`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Update Layer Style](https://developers.felt.com/rest-api/api-reference/layers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map where the layer is located. |
| `layerId` | path | `string` | yes | The ID of the layer to update. |
| `style` | body | `object` | yes | The new layer style in Felt Style Language format. |
