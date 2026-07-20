# Update Product with Voog

Updates an existing product in the current Voog store.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ecommerce/v1/products/:productId`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Update Product](https://www.voog.com/developers/api/ecommerce/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product.name` | body | `string` | yes | Updated product name. |
| `product.price` | body | `number` | yes | Updated product price. |
| `product.status` | body | `string` | yes | Updated product status. |
| `productId` | path | `number` | yes | Numeric product ID. |
