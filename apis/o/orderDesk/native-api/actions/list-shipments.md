# List Shipments with Order Desk

Retrieves shipments from Order Desk.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:orderId/shipments`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [List Shipments](https://apidocs.orderdesk.com/?shell=#get-all-shipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order Desk internal order ID. |
