# Update Variant with Katana

Updates an existing variant in Katana.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/variants/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Variant](https://developer.katanamrp.com/reference/updatevariant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Variant id |
| `sku` | body | `string` | no | — |
| `sales_price` | body | `number` | no | — |
| `purchase_price` | body | `number` | no | — |
| `product_id` | body | `number` | no | — |
| `supplier_item_codes[]` | body | `array<string>` | no | — |
| `internal_barcode` | body | `string` | no | Maximum length: 40. |
| `registered_barcode` | body | `string` | no | Maximum length: 120. |
| `material_id` | body | `number` | no | — |
| `lead_time` | body | `number` | no | — |
| `minimum_order_quantity` | body | `number` | no | — |
| `config_attributes[]` | body | `array<object>` | no | — |
| `config_attributes[].config_name` | body | `string` | no | If a matching config name is not found, an error is returned.               Use the product/material endpoint to update the configs. |
| `config_attributes[].config_value` | body | `string` | no | If a matching config name is not found,               the product/material config list of values is updated, and a new value is added. |
| `custom_fields[]` | body | `array<object>` | no | — |
| `custom_fields[].field_name` | body | `string` | no | Maximum length: 40. |
| `custom_fields[].field_value` | body | `string` | no | Maximum length: 100. |
