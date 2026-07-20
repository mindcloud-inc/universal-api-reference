# Create Shipment with Order Desk

Creates a new shipment in Order Desk.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/:orderId/shipments`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Create Shipment](https://apidocs.orderdesk.com/?shell=#create-a-shipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order Desk internal order ID. |
| `tracking_number` | body | `string` | yes | Carrier tracking number for the shipment. |
| `carrier_code` | body | `string` | no | Carrier code such as UPS or USPS. |
| `shipment_method` | body | `string` | no | Shipment service or method label. |
