# Update Order Status with Stockpilot

Updates an order status in Stockpilot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/orders/:order_id/update-status`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Update Order Status](https://api.stockpilot.dev/redoc#operation/update_order_status_orders__order_id__update_status_patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | path | `number` | yes |
| `status` | body | `string` | yes |
