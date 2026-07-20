# Update Orders with Extensiv Order Manager

Updates orders in Extensiv Order Manager.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.1/orders`
- **Base URL:** `https://api.skubana.com`
- **Official documentation:** [Update Orders](https://documentation.skubana.com/pages/order-manager.html#tag/Order/operation/postOrderUsingPOST_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amountPaid` | body | `object` | no | — |
| `amountPaid.amount` | body | `number` | no | — |
| `customShipBilling.accountNumber` | body | `string` | no | — |
| `customShipBilling.codAmount.amount` | body | `number` | no | — |
| `fulfillmentSource.name` | body | `string` | no | — |
| `orderIdentifier.orderId` | body | `number` | no | — |
| `shipMethod.ltlFtlShipment` | body | `object` | no | Less Than Truckload Full Truckload Shipment |
| `shipMethod.ltlFtlShipment.boxCount` | body | `number` | no | — |
| `amountPaid.currency` | body | `string` | no | — |
| `customField1` | body | `string` | no | — |
| `customShipBilling.billingZipCode` | body | `string` | no | — |
| `customShipBilling.codAmount.currency` | body | `string` | no | — |
| `fulfillmentSource.warehouseId` | body | `number` | no | — |
| `orderIdentifier.orderNumber` | body | `string` | no | — |
| `shipMethod.ltlFtlShipment.freightReadyDate` | body | `string` | no | — |
| `shipMethod.shippingCarrier` | body | `string` | no | — |
| `customField2` | body | `string` | no | — |
| `customShipBilling.codAmount` | body | `object` | no | — |
| `orderIdentifier.salesChannelId` | body | `number` | no | — |
| `shipMethod.ltlFtlShipment.id` | body | `number` | no | — |
| `shipMethod.shippingProviderId` | body | `number` | no | — |
| `customField3` | body | `string` | no | — |
| `customShipBilling.country` | body | `string` | no | — |
| `shipMethod.ltlFtlShipment.liabilityCoverage` | body | `number` | no | — |
| `shipMethod.shippingServiceId` | body | `number` | no | — |
| `customShipBilling` | body | `object` | no | — |
| `shipMethod.ltlFtlShipment.liabilityType` | body | `string` | no | — |
| `shipMethod.packageTypeId` | body | `number` | no | — |
| `customShipBillingOption` | body | `list<string>` | no | — |
| `shipMethod.ltlFtlShipment.measurementUnitId` | body | `number` | no | — |
| `fulfillmentSource` | body | `object` | no | — |
| `gift` | body | `boolean` | no | — |
| `giftMessage` | body | `string` | no | Maximum length: 1000. |
| `height` | body | `number` | no | Maximum length: 0. |
| `internalNotes` | body | `string` | no | — |
| `length` | body | `number` | no | — |
| `orderIdentifier` | body | `object` | no | — |
| `paymentDate` | body | `string` | no | — |
| `receiveByDate` | body | `string` | no | — |
| `shipAddress1` | body | `string` | no | — |
| `shipAddress2` | body | `string` | no | — |
| `shipAddress3` | body | `string` | no | — |
| `shipByDate` | body | `string` | no | — |
| `shipCity` | body | `string` | no | — |
| `shipCompany` | body | `string` | no | — |
| `shipCountry` | body | `string` | no | — |
| `shipMethod` | body | `object` | no | — |
| `shipName` | body | `string` | no | — |
| `shipPhone` | body | `string` | no | — |
| `shipState` | body | `string` | no | — |
| `shipZipCode` | body | `string` | no | — |
| `weight` | body | `number` | no | — |
| `width` | body | `number` | no | — |
