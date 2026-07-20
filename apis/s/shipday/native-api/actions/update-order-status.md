# Update Order Status with Shipday

Updates an existing order status in Shipday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/:orderId/status`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Update Order Status](https://docs.shipday.com/reference/order-status-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Shipday order ID used in the request path. |
| `status` | body | `string` | yes | Delivery status value sent in the request body. |
