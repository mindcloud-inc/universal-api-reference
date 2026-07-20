# Stock Availability with Gelato

Retrieves regional stock availability for Gelato products.

## Endpoint

- **Method:** `POST`
- **Path:** `https://product.gelatoapis.com/v3/stock/region-availability`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Stock Availability](https://dashboard.gelato.com/docs/products/stock/region-availability/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `products[]` | body | `array<string>` | yes |
