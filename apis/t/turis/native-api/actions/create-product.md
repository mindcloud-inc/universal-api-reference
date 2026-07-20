# Create Product with Turis

Creates a new product in Turis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v1/products`
- **Base URL:** `https://{tenant}.turis.app`
- **Official documentation:** [Create Product](https://documenter.getpostman.com/view/16452985/TzkyP1Er)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_quantity` | body | `number` | yes | Case quantity for the product. |
| `category_id` | body | `list<number>` | yes | Primary category ID. |
| `category_ids[]` | body | `array<number>` | yes | Product category IDs. |
| `currentPrice[].currency_id` | body | `number` | no | Currency for the current price. |
| `currentPrice[].price` | body | `number` | no | Current price amount. |
| `is_product_free` | body | `boolean` | no | Whether the product is free. |
| `is_shown` | body | `boolean` | no | Whether the product is shown. |
| `name` | body | `string` | yes | Product name. |
| `recommendedRetailPrice[].currency_id` | body | `number` | no | Currency for the recommended retail price. |
| `recommendedRetailPrice[].price` | body | `number` | no | Recommended retail price amount. |
| `sku` | body | `string` | yes | Product SKU. |
| `stock` | body | `number` | yes | Initial stock quantity. |
| `supplier` | body | `string` | no | Product supplier. |
| `unit_cost` | body | `number` | yes | Unit cost of the product. |
