# Update Product Category with Dukaan

Updates an existing product category in Dukaan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `api/product/seller/:categoryUuid/product-category/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Update Product Category](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryUuid` | path | `string` | yes | Dukaan category UUID from the category record. |
| `name` | body | `string` | no | Category name. |
| `store` | body | `string` | no | Store UUID or ID for the category. |
| `show_to` | body | `number` | no | Dukaan visibility value for the category. |
| `description` | body | `string` | no | Category description HTML. |
| `product_add[]` | body | `array<number>` | no | Product IDs to add to the category. |
| `product_remove[]` | body | `array<number>` | no | Product IDs to remove from the category. |
