# Link Products to Orders with Revi.io Reviews

Links products to orders in Revi.io Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders_products`
- **Base URL:** `https://api.revi.io/api/v1`
- **Official documentation:** [Link Products to Orders](https://docs.revi7.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders_products[]` | body | `array<object>` | yes | Array linking each order to one or more purchased products. |
