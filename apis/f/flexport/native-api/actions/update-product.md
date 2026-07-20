# Update Product with Flexport

Updates an existing product in Flexport.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/products/:id`
- **Base URL:** `https://api.flexport.com`
- **Official documentation:** [Update Product](https://apidocs.flexport.com/2023-07-01/tag/Product#operation/products_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique Flexport product ID to update. |
| `name` | body | `string` | no | Product name. |
| `sku` | body | `string` | no | Product SKU. |
| `description` | body | `string` | no | Product description. |
