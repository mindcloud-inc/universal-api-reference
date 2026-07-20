# Create Variant with Katana

Creates a new variant in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/variants`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Create Variant](https://developer.katanamrp.com/reference/create-variant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
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
| `config_attributes[].config_name` | body | `string` | no | — |
| `config_attributes[].config_value` | body | `string` | no | — |
| `custom_fields[]` | body | `array<object>` | no | — |
| `custom_fields[].field_name` | body | `string` | no | Maximum length: 40. |
| `custom_fields[].field_value` | body | `string` | no | Maximum length: 100. |
