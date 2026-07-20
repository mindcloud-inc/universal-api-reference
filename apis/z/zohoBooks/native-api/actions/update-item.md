# Update Item with Zoho Books

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:item_id`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Update Item](https://www.zoho.com/books/api/v3/items/#update-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `list` | yes | — |
| `organization_id` | query | `list` | yes | — |
| `name` | body | `string` | yes | Maximum length: 100. |
| `rate` | body | `number` | yes | — |
| `description` | body | `string` | no | Maximum length: 2000. |
| `sku` | body | `string` | no | — |
| `product_type` | body | `list` | no | Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `item_type` | body | `list` | no | Accepted values: `0`, `1`, `2`, `3`. |
| `tax_id` | body | `string` | no | — |
| `is_taxable` | body | `boolean` | no | — |
| `tax_exemption_id` | body | `string` | no | — |
| `account_id` | body | `string` | no | — |
| `purchase_description` | body | `string` | no | — |
| `purchase_rate` | body | `number` | no | — |
| `purchase_account_id` | body | `string` | no | — |
| `inventory_account_id` | body | `string` | no | — |
| `vendor_id` | body | `string` | no | — |
| `reorder_level` | body | `number` | no | — |
| `locations[]` | body | `array<object>` | no | — |
| `locations[].location_id` | body | `string` | no | — |
| `locations[].initial_stock` | body | `number` | no | — |
| `locations[].initial_stock_rate` | body | `number` | no | — |
