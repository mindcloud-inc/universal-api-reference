# Search Products with Quizell

Finds products in Quizell by title or SKU.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/search`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Search Products](https://docs.quizell.com/product-apis#search-product)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | no | Product title to search for. |
| `sku` | query | `string` | no | Product SKU to search for. |
| `status` | query | `number` | no | Product status: 1 for active, 0 for inactive. |
