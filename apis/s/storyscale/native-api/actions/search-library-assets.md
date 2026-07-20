# Search Library Assets with Storyscale

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/library/search`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Search Library Assets](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_type_id` | query | `number` | no | Filter by library asset type. |
| `is_favourite` | query | `boolean` | no | Filter to favourite assets. |
| `is_splash_image` | query | `boolean` | no | Filter to splash-image assets. |
| `search-val` | query | `string` | no | Filter library assets by a search string. |
