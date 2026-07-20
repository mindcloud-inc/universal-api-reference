# Update Custom Field with Gumroad

Updates an existing custom field in Gumroad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:product_id/custom_fields/:name`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Update Custom Field](https://gumroad.com/api#put-/products/:product_id/custom_fields/:name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
| `name` | path | `string` | yes | The custom field name. |
| `required` | body | `boolean` | no | Whether the custom field is required. |
| `variant` | body | `string` | no | The variant this custom field applies to, when applicable. |
