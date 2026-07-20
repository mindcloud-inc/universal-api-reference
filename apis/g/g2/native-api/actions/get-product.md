# Get Product with G2

Retrieves a product from G2.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/products/:product_id`
- **Base URL:** `https://data.g2.com`
- **Official documentation:** [Get Product](https://data.g2.com/openapi/v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | Product UUID or slug from the G2 API spec. |
