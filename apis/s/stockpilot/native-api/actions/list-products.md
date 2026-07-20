# List Products with Stockpilot

Retrieves products from Stockpilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [List Products](https://api.stockpilot.dev/redoc#operation/get_product_list_products_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `page_size` | query | `number` | no | Items per page |
