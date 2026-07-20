# Update Shipment with Order Desk

Updates an existing shipment in Order Desk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/:orderId/shipments/:shipmentId`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Update Shipment](https://apidocs.orderdesk.com/?shell=#update-a-shipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order Desk internal order ID. |
| `shipmentId` | path | `string` | yes | Order Desk internal shipment ID. |
| `tracking_number` | body | `string` | yes | Carrier tracking number for the shipment. |
| `carrier_code` | body | `string` | no | Carrier code such as UPS or USPS. |
| `shipment_method` | body | `string` | no | Shipment service or method label. |
