# Get Catalog Items with Pinterest

Retrieves catalog items from Pinterest.

## Endpoint

- **Method:** `POST`
- **Path:** `catalogs/items`
- **Base URL:** `https://api.pinterest.com/v5`
- **Official documentation:** [Get Catalog Items](https://developers.pinterest.com/docs/api/v5/#operation/items/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `country` | body | `string` | no |
| `filters.catalog_type` | body | `string` | no |
| `filters.item_ids` | body | `array<string>` | no |
| `language` | body | `string` | no |
| `filters` | body | `object` | no |
| `filters.catalog_id` | body | `string` | no |
