# Create Product with Stockpilot

Creates a new product in Stockpilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/create`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Create Product](https://api.stockpilot.dev/redoc#operation/create_product_products_create_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Product title |
| `description` | body | `string` | no | Product description |
| `brand` | body | `number` | no | Brand ID |
| `category` | body | `number` | no | Category ID |
| `is_active` | body | `boolean` | no | Whether the product is active |
