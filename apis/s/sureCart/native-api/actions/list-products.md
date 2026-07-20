# List Products with SureCart

## Endpoint

- **Method:** `GET`
- **Path:** `v1/products`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [List Products](https://developer.surecart.com/api-reference/products/list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Full-text search query for the product collection. |
| `archived` | query | `boolean` | no | Only return archived or active products. |
| `featured` | query | `boolean` | no | Only return featured or non-featured products. |
| `recurring` | query | `boolean` | no | Only return recurring or one-time products. |
