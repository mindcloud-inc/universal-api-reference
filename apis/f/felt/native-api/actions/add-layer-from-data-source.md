# Add Layer From Data Source with Felt

Creates a map layer from a data source in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/add_source_layer`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Add Layer From Data Source](https://developers.felt.com/rest-api/api-reference/layers/layer-uploads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | Map ID that will receive the new layer. |
| `from` | body | `string` | yes | Source-layer creation mode: dataset, sql, or stac. |
| `dataset_id` | body | `string` | no | Dataset ID when from=dataset. |
| `source_id` | body | `string` | no | Source ID when from=sql or from=stac. |
| `query` | body | `string` | no | SQL query when from=sql. |
| `stac_asset_url` | body | `string` | no | STAC asset URL when from=stac. |
