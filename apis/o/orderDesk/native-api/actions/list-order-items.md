# List Order Items with Order Desk

Retrieves order items from Order Desk.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:orderId/order-items`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [List Order Items](https://apidocs.orderdesk.com/?shell=#get-all-order-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order Desk internal order ID. |
