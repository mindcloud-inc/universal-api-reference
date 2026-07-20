# Update Product with Invoice Ninja

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:id`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Update Product](https://api-docs.invoicing.co/#tag/products/operation/updateProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hashed product ID. |
| `product_key` | body | `string` | yes | Invoice Ninja product key. |
| `notes` | body | `string` | no | Notes or description for the product. |
| `cost` | body | `number` | yes | Product cost. |
| `price` | body | `number` | yes | Product price. |
| `quantity` | body | `number` | no | Product quantity. |
