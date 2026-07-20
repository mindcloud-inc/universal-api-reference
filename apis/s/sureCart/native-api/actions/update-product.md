# Update Product with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/products/:id`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Update Product](https://developer.surecart.com/api-reference/products/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The product ID to update. |
| `product.name` | body | `string` | no | The updated product name. |
