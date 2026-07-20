# Update Product with TrackMage

Updates an existing product in TrackMage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/{id}`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Update Product](https://docs.trackmage.com/docs/product/product.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource identifier |
| `name` | body | `string` | no | The name of product. |
| `sku` | body | `string` | no | The SKU of product. |
| `originUrl` | body | `string` | no | The URL of product in the ecommerce store. |
| `imageUrl` | body | `string` | no | The URL of product image in the ecommerce store. |
