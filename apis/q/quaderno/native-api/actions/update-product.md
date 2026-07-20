# Update Product with Quaderno

Updates an existing product in Quaderno.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:id`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Update Product](https://developers.quaderno.io/api/#tag/Products/operation/updateProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated product description. |
| `id` | path | `string` | yes | ID of the product to update. |
| `unit_cost` | body | `string` | no | Updated unit cost. |
