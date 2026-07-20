# Create Product with Quizell

Creates a new product in Quizell.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/store`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Create Product](https://docs.quizell.com/product-apis#create-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | body | `boolean` | yes | Product active status. |
| `title` | body | `string` | yes | Product title. |
| `price` | body | `number` | yes | Product price. |
| `description` | body | `string` | no | Product description. |
| `image` | body | `string` | no | Product image URL. |
| `tags[]` | body | `array<string>` | no | Product tags. |
| `sku` | body | `string` | no | Product SKU. |
| `quantity` | body | `number` | no | Available quantity. |
