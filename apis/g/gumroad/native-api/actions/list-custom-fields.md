# List Custom Fields with Gumroad

Retrieves custom fields for a Gumroad product.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:product_id/custom_fields`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [List Custom Fields](https://gumroad.com/api#get-/products/:product_id/custom_fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
