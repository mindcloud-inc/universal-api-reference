# Create Standard Shipment with Extensiv Order Manager

Creates a standard shipment in Extensiv Order Manager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.1/shipment/standard`
- **Base URL:** `https://api.skubana.com`
- **Official documentation:** [Create Standard Shipment](https://documentation.skubana.com/pages/order-manager.html#tag/Shipment/operation/putShipmentUsingPUT_1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `completeBatchAndDiscardFailedOrders` | body | `boolean` | no |
| `orderBatchNumber` | body | `number` | no |
| `orderIds[]` | body | `array<number>` | yes |
