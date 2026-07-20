# Update Product with Katana

Updates an existing product in Katana.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/products/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Product](https://developer.katanamrp.com/reference/updateproduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Product id |
| `name` | body | `string` | no | — |
| `uom` | body | `string` | no | Maximum length: 7. |
| `category_name` | body | `string` | no | — |
| `is_sellable` | body | `boolean` | no | — |
| `is_producible` | body | `boolean` | no | A product has to be purchasable, producible, or both. |
| `is_purchasable` | body | `boolean` | no | A product has to be purchasable, producible, or both. |
| `is_auto_assembly` | body | `boolean` | no | A product can be auto-assembled only if it is producible and not batch tracked. |
| `is_archived` | body | `boolean` | no | — |
| `default_supplier_id` | body | `number` | no | — |
| `additional_info` | body | `string` | no | — |
| `batch_tracked` | body | `boolean` | no | — |
| `operations_in_sequence` | body | `boolean` | no | — |
| `serial_tracked` | body | `boolean` | no | — |
| `purchase_uom` | body | `string` | no | If used, then purchase_uom_conversion_rate must have a value as well. Maximum length: 7. |
| `purchase_uom_conversion_rate` | body | `number` | no | If used, then purchase_uom must have a value as well. |
| `configs[]` | body | `array<object>` | no | When updating configs, all configs and values must be provided.         Existing ones are matched, new ones are created, and configs not provided in the update are deleted. |
| `configs[].id` | body | `number` | no | If config ID is used to map the config, then name is ignored. |
| `configs[].name` | body | `string` | no | If config name is used to map the config, then we match to the existing config by name.               If a match is not found, a new one is created. |
| `configs[].values[]` | body | `array<string>` | no | — |
| `custom_field_collection_id` | body | `number` | no | — |
