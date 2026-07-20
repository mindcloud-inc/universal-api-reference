# Get Item Sales Analytics with Stockpilot

Retrieves item sales analytics from Stockpilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/items/sales`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Get Item Sales Analytics](https://api.stockpilot.dev/redoc#operation/get_item_sales_analytics_analytics_items_sales_get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `number` | no |
| `sku` | query | `string` | no |
| `barcode` | query | `string` | no |
| `range` | query | `number` | no |
| `include_channels` | query | `boolean` | no |
| `metrics` | query | `string` | no |
