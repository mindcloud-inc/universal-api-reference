# Update Shipment Item with TrackMage

Updates an existing shipment item in TrackMage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/shipment_items/{id}`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Update Shipment Item](https://docs.trackmage.com/docs/shipment/shipment-item.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource identifier |
| `orderItem` | body | `string` | yes | The order item reference to which the shipment items item belongs. |
| `qty` | body | `number` | no | The number of items in the shipment. Default and the minimum value is 0. The value cannot be greater than available quantity of the order item (orderItem.qty - orderItem.fulfilledQty). |
