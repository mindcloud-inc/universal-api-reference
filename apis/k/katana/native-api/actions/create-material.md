# Create Material with Katana

Creates a new material in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/materials`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Create Material](https://developer.katanamrp.com/reference/creatematerial)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `uom` | body | `string` | no | Maximum length: 7. |
| `category_name` | body | `string` | no | — |
| `default_supplier_id` | body | `number` | no | — |
| `additional_info` | body | `string` | no | — |
| `batch_tracked` | body | `boolean` | no | — |
| `is_sellable` | body | `boolean` | no | — |
| `purchase_uom` | body | `string` | no | Maximum length: 7. |
| `purchase_uom_conversion_rate` | body | `number` | no | — |
| `configs[]` | body | `array<object>` | no | — |
| `configs[].name` | body | `string` | no | — |
| `configs[].values[]` | body | `array<string>` | no | — |
| `custom_field_collection_id` | body | `number` | no | — |
| `variants[]` | body | `array<object>` | yes | — |
| `variants[].sku` | body | `string` | no | — |
| `variants[].purchase_price` | body | `number` | no | — |
| `variants[].internal_barcode` | body | `string` | no | Maximum length: 40. |
| `variants[].registered_barcode` | body | `string` | no | Maximum length: 40. |
| `variants[].supplier_item_codes[]` | body | `array<string>` | no | — |
| `variants[].lead_time` | body | `number` | no | — |
| `variants[].minimum_order_quantity` | body | `number` | no | — |
| `variants[].config_attributes[]` | body | `array<object>` | no | — |
| `variants[].config_attributes[].config_name` | body | `string` | no | — |
| `variants[].config_attributes[].config_value` | body | `string` | no | — |
| `variants[].custom_fields[]` | body | `array<object>` | no | — |
| `variants[].custom_fields[].field_name` | body | `string` | no | Maximum length: 40. |
| `variants[].custom_fields[].field_value` | body | `string` | no | Maximum length: 100. |
