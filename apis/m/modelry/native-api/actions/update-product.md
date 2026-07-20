# Update Product with Modelry

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/products/:id`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Update Product](https://files.cgtarsenal.com/api/doc/index.html#api-Products-UpdateProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Modelry product ID. |
| `product.title` | body | `string` | yes | Product title from Modelry docs. |
| `product.sku` | body | `string` | yes | Unique product SKU. |
| `product.description` | body | `string` | yes | Product description. |
| `product.batch_id` | body | `string` | yes | Modeling batch identifier. |
| `product.tags[]` | body | `array<string>` | yes | Array of product tags. |
| `product.dimensions` | body | `string` | yes | Product dimensions string. |
| `product.external_url` | body | `string` | yes | External product URL. |
