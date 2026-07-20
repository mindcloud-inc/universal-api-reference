# Browse Product Buyer Intent with G2

Retrieves buyer intent interactions for a product in G2.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/products/:subject_product_id/buyer_intent`
- **Base URL:** `https://data.g2.com`
- **Official documentation:** [Browse Product Buyer Intent](https://data.g2.com/openapi/v2.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimensions` | query | `string` | no | Comma-separated list of buyer intent dimensions. |
| `measures` | query | `string` | no | Comma-separated list of buyer intent measures. |
| `sort` | query | `string` | no | Sort field with optional leading minus for descending order. |
| `subject_product_id` | path | `string` | yes | Product UUID for scoped buyer intent. |
