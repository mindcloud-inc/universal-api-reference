# List Shipments with Extensiv Order Manager

Retrieves shipments from Extensiv Order Manager.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/shipments`
- **Base URL:** `https://api.skubana.com`
- **Official documentation:** [List Shipments](https://documentation.skubana.com/pages/order-manager.html#tag/Shipment/operation/getShipmentsUsingGET)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `batchNumber` | query | `string` | no |
| `city` | query | `string` | no |
| `country` | query | `string` | no |
| `deliveryStatus` | query | `list<string>` | no |
| `orderId[]` | query | `array<number>` | no |
| `orderNumber[]` | query | `array<string>` | no |
| `recipient` | query | `string` | no |
| `salesChannelId` | query | `number` | no |
| `shipmentCreatedFromDate` | query | `string` | no |
| `shipmentCreatedToDate` | query | `string` | no |
| `shipmentFromDate` | query | `string` | no |
| `shipmentId[]` | query | `array<number>` | no |
| `shipmentToDate` | query | `string` | no |
| `shippingProviderId` | query | `number` | no |
| `state` | query | `string` | no |
| `trackingNumber` | query | `string` | no |
| `warehouseId` | query | `number` | no |
