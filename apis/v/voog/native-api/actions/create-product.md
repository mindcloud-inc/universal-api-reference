# Create Product with Voog

Creates a new product in the current Voog store.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/v1/products`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Create Product](https://www.voog.com/developers/api/ecommerce/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product.name` | body | `string` | yes | Product name in the current language. |
| `product.price` | body | `number` | yes | Product price. |
| `product.slug` | body | `string` | yes | Product URL slug. |
| `product.status` | body | `string` | yes | Product status. |
