# Create Multiple Shipments with Order Desk

Creates multiple shipments in Order Desk.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch-shipments`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Create Multiple Shipments](https://apidocs.orderdesk.com/?shell=#create-multiple-shipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipments[].order_id` | body | `string` | yes | Order Desk internal order ID for the shipment target. |
| `shipments[].tracking_number` | body | `string` | yes | Carrier tracking number for the shipment. |
| `shipments[].carrier_code` | body | `string` | no | Carrier code such as UPS or USPS. |
| `shipments[].shipment_method` | body | `string` | no | Shipment service or method label. |
