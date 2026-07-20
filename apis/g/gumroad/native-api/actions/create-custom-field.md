# Create Custom Field with Gumroad

Creates a new custom field in Gumroad.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/:product_id/custom_fields`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Create Custom Field](https://gumroad.com/api#post-/products/:product_id/custom_fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
| `name` | body | `string` | yes | The custom field name. |
| `required` | body | `boolean` | yes | Whether the custom field is required. |
| `variant` | body | `string` | no | The variant this custom field applies to, when applicable. |
