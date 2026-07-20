# Create External Shipment with Extensiv Order Manager

Creates an external shipment in Extensiv Order Manager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.1/shipment/external`
- **Base URL:** `https://api.skubana.com`
- **Official documentation:** [Create External Shipment](https://documentation.skubana.com/pages/order-manager.html#tag/Shipment/operation/putExternalShipmentUsingPUT_1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `notifyCustomer` | body | `boolean` | no |
| `shipments[].carrierFee.amount` | body | `number` | no |
| `shipments[].shipMethod.shippingCarrier` | body | `string` | yes |
| `shipments[].trackingNumber` | body | `string` | yes |
| `shipments[].carrierFee.currency` | body | `string` | no |
| `shipments[].shipMethod` | body | `object` | yes |
| `shipments[].shipMethod.packageTypeId` | body | `number` | no |
| `updateChannel` | body | `boolean` | no |
| `shipments[]` | body | `array<object>` | yes |
| `shipments[].carrierFee` | body | `object` | no |
| `shipments[].shipMethod.shippingServiceId` | body | `number` | no |
| `shipments[].deliveryStatus` | body | `list<string>` | no |
| `shipments[].estimatedArrival` | body | `string` | no |
| `shipments[].insuranceTrackingNumber` | body | `string` | no |
| `shipments[].orderId` | body | `number` | no |
| `shipments[].orderNumber` | body | `string` | no |
| `shipments[].received` | body | `string` | no |
| `shipments[].salesChannelId` | body | `string` | no |
| `shipments[].shipDate` | body | `string` | no |
