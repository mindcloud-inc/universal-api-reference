# Update Product with Quizell

Updates an existing product in Quizell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/update/:product_id`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Update Product](https://docs.quizell.com/product-apis#update-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | The ID of the product to update. |
| `status` | body | `boolean` | no | Product active status. |
| `title` | body | `string` | no | Product title. |
| `price` | body | `number` | no | Product price. |
| `description` | body | `string` | no | Product description. |
| `image` | body | `string` | no | Product image URL. |
| `tags[]` | body | `array<string>` | no | Product tags. |
| `sku` | body | `string` | no | Product SKU. |
