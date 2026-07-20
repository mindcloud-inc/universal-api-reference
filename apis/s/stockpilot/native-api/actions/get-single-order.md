# Get Single Order with Stockpilot

Retrieves an order from Stockpilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/get-single`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Get Single Order](https://api.stockpilot.dev/redoc#operation/get_single_order_orders_get_single_get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_pk` | query | `number` | no |
| `order_number` | query | `string` | no |
