# Create Shipment Item with TrackMage

Creates a new shipment item in TrackMage.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipment_items`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Create Shipment Item](https://docs.trackmage.com/docs/shipment/shipment-item.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipment` | body | `object` | yes | — |
| `orderItem` | body | `string` | yes | The order item reference to which the shipment items item belongs. |
| `qty` | body | `number` | no | The number of items in the shipment. Default and the minimum value is 0. The value cannot be greater than available quantity of the order item (orderItem.qty - orderItem.fulfilledQty). |
| `externalSourceSyncId` | body | `string` | no | The id of the shipment item in ecommerce store (WooCommerce, Shopify, etc.). |
| `externalSourceIntegration` | body | `string` | no | The workflow reference to integration for ecommerce store. |
| `fulfillmentIntegration` | body | `string` | no | The workflow reference to integration for fulfillment source. |
| `fulfillmentSyncId` | body | `string` | no | The id of the shipment item in the fulfillment source system (AliExpress, Amazon, etc.). |
