# Link Full Products to Orders with Revi.io Reviews

Links full products to orders in Revi.io Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders_products`
- **Base URL:** `https://api.revi.io/api/v1`
- **Official documentation:** [Link Full Products to Orders](https://docs.revi7.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders_products[]` | body | `array<object>` | yes | Array linking orders to full product objects that should be created inline. |
