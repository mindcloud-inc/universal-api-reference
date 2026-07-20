# Delete Custom Field with Gumroad

Deletes an existing custom field from Gumroad.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products/:product_id/custom_fields/:name`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Delete Custom Field](https://gumroad.com/api#delete-/products/:product_id/custom_fields/:name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
| `name` | path | `string` | yes | The custom field name. |
