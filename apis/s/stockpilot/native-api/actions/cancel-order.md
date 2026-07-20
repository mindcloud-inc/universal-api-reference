# Cancel Order with Stockpilot

Updates an order as canceled in Stockpilot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/cancel-order`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Cancel Order](https://api.stockpilot.dev/redoc#operation/cancel_order_orders_cancel_order_put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_pk` | body | `number` | yes |
| `reason_code` | body | `string` | no |
