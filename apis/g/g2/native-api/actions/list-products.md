# List Products with G2

Retrieves products from G2.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/products`
- **Base URL:** `https://data.g2.com`
- **Official documentation:** [List Products](https://data.g2.com/openapi/v2.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[product_name_cont]` | query | `string` | no | Filter products by partial name match. |
| `filter[product_name_eq]` | query | `string` | no | Filter products by exact name match. |
| `filter[query]` | query | `string` | no | Full-text product search query. |
| `filter[vendor_name]` | query | `string` | no | Filter products by vendor name. |
