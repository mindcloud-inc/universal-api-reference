# Get Variant Watchlist with Frameshift

Retrieves the variant watchlist from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/variants/sets/watchlist`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Get Variant Watchlist](https://mosaic.frameshift.io/api/#api-Variants-GetVariantWatchlist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `include_variant_data` | query | `boolean` | no | If true, all data for the variants in the watchlist will be returned. |
| `include_genotype_data` | query | `boolean` | no | If true, genotype data will be returned. |
