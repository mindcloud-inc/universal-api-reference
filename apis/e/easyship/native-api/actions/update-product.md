# Update Product with Easyship

Updates an existing product in Easyship.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/products/:product_id`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Update Product](https://developers.easyship.com/reference/products_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The Easyship product ID. |
| `identifier` | body | `string` | no | SKU for the product. |
| `name` | body | `string` | no | Human-readable name of the product. |
| `comments` | body | `string` | no | Optional comments for the product. |
| `input_type` | body | `string` | no | Product input type. |
| `length` | body | `number` | no | Length of the product in centimeters. |
| `width` | body | `number` | no | Width of the product in centimeters. |
| `height` | body | `number` | no | Height of the product in centimeters. |
| `weight` | body | `number` | no | Weight of the product in kilograms. |
| `item_category_id` | body | `number` | no | Item category ID. |
| `store_id` | body | `string` | no | Store ID. |
| `platform_product_id` | body | `string` | no | Platform product ID. |
| `cost_price` | body | `number` | no | Product cost price. |
| `cost_price_currency` | body | `string` | no | Product cost currency. |
| `selling_price` | body | `number` | no | Product selling price. |
| `selling_price_currency` | body | `string` | no | Product selling price currency. |
| `image_url` | body | `string` | no | Product image URL. |
| `pick_location` | body | `string` | no | Pickup location for the product. |
| `origin_country_alpha2` | body | `string` | no | Country where the product is manufactured. |
| `hs_code` | body | `string` | no | Harmonized System code for customs. |
| `contains_liquids` | body | `boolean` | no | Whether the product contains liquids. |
| `contains_battery_pi966` | body | `boolean` | no | Whether the product applies packing instruction 966. |
| `contains_battery_pi967` | body | `boolean` | no | Whether the product applies packing instruction 967. |
