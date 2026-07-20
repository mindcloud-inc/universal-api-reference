# Delete Shipment with Order Desk

Deletes an existing shipment from Order Desk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orders/:orderId/shipments/:shipmentId`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Delete Shipment](https://apidocs.orderdesk.com/?shell=#delete-a-shipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order Desk internal order ID. |
| `shipmentId` | path | `string` | yes | Order Desk internal shipment ID. |
