# Update Product with JoggAI

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/product`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Update Product](https://docs.jogg.ai/api-reference/v2/Product/UpdateProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated product description |
| `name` | body | `string` | no | Updated product name |
| `product_id` | body | `string` | yes | Product ID to update |
| `target_audience` | body | `string` | no | Updated target audience |
