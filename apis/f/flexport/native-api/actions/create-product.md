# Create Product with Flexport

Creates a new product in Flexport.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://api.flexport.com`
- **Official documentation:** [Create Product](https://apidocs.flexport.com/2023-07-01/tag/Product#operation/products_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Product name. |
| `sku` | body | `string` | yes | Unique product SKU. |
