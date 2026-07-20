# Create Custom Layer Export with Felt

Creates a custom layer export in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/layers/:layerId/custom_export`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Create Custom Layer Export](https://developers.felt.com/rest-api/api-reference/layers/layer-exports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map where the layer is located. |
| `layerId` | path | `string` | yes | The ID of the layer to export. |
| `output_format` | body | `list` | yes | The export output format. Accepted values: `CSV`, `GeoJSON`, `GeoPackage`, `GeoTIFF`. |
| `email_on_completion` | body | `boolean` | no | Whether Felt should email when the export completes. |
| `filters[]` | body | `array<object>` | no | Optional Felt Style Language filters for the export. |
