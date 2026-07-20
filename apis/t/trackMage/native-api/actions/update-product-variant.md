# Update Product Variant with TrackMage

Updates an existing product variant in TrackMage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/product_variants/{id}`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Update Product Variant](https://docs.trackmage.com/docs/product/product-variant.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource identifier |
| `imageUrl` | body | `string` | no | The URL of product variant image in the ecommerce store. |
| `price` | body | `string` | no | The price of product variant in the store currency. Default value is **0** |
