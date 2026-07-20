# Get Shipment with Order Desk

Retrieves a shipment from Order Desk.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:orderId/shipments/:shipmentId`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Get Shipment](https://apidocs.orderdesk.com/?shell=#get-a-single-shipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order Desk internal order ID. |
| `shipmentId` | path | `string` | yes | Order Desk internal shipment ID. |
