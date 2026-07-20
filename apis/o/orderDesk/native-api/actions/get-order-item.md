# Get Order Item with Order Desk

Retrieves an order item from Order Desk.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:orderId/order-items/:orderItemId`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Get Order Item](https://apidocs.orderdesk.com/?shell=#get-a-single-order-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order Desk internal order ID. |
| `orderItemId` | path | `string` | yes | Order Desk internal order item ID. |
