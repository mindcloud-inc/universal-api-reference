# Create a Product with Jetbuilt

## Endpoint

- **Method:** `POST`
- **Path:** `product_databases/:productDatabaseId/products`
- **Base URL:** `https://app.jetbuilt.com/api/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commodity_code` | body | `string` | no | — |
| `cost` | body | `number` | no | — |
| `country_of_origin` | body | `string` | no | — |
| `currency_code` | body | `string` | no | — |
| `depth_unit` | body | `string` | no | Possible values: in, ft, cm, mm |
| `depth_value` | body | `number` | no | — |
| `favorite` | body | `string` | no | — |
| `heat_load_unit` | body | `string` | no | Possible values: BTU |
| `heat_load_value` | body | `string` | no | — |
| `height_unit` | body | `string` | no | Possible values: in, ft, cm, mm |
| `height_value` | body | `number` | no | — |
| `image` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `phase_id` | body | `string` | no | — |
| `poe_unit` | body | `string` | no | Possible values: W |
| `poe_value` | body | `number` | no | — |
| `power_unit` | body | `string` | no | Possible values: W |
| `power_value` | body | `number` | no | — |
| `Price` | body | `number` | no | — |
| `product_id` | body | `number` | no | — |
| `rack_unit` | body | `string` | no | Possible values: RU |
| `rack_value` | body | `number` | no | — |
| `shipping_cost` | body | `string` | no | — |
| `shipping_depth_unit` | body | `string` | no | Possible values: in, ft, cm, mm |
| `shipping_depth_value` | body | `number` | no | — |
| `shipping_height_unit` | body | `string` | no | Possible values: in, ft, cm, mm |
| `shipping_height_value` | body | `number` | no | — |
| `shipping_price` | body | `number` | no | — |
| `shipping_weight_unit` | body | `string` | no | Possible values: lb, oz, kg, g |
| `shipping_weight_value` | body | `number` | no | — |
| `shipping_width_unit` | body | `string` | no | Possible values: in, ft, cm, mm |
| `shipping_width_value` | body | `number` | no | — |
| `short_description` | body | `string` | no | — |
| `tax_equipment` | body | `boolean` | no | — |
| `tax_labor` | body | `boolean` | no | — |
| `tax_shipping` | body | `boolean` | no | — |
| `warranty_unit` | body | `string` | no | Possible values: d, mo, yr |
| `warranty_value` | body | `number` | no | The warranty value in days months or years (decimal) |
| `weight_unit` | body | `string` | no | Possible values: lb, oz, kg, g |
| `weight_value` | body | `number` | no | — |
| `width_unit` | body | `string` | no | Possible values: in, ft, cm, mm |
| `width_value` | body | `number` | no | — |
| `productDatabaseId` | path | `string` | yes | — |
| `manufacturer_name` | body | `string` | no | — |
| `model` | body | `string` | no | — |
