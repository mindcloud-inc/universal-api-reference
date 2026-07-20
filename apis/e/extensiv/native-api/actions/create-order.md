# Create Order with Extensiv Order Manager

Creates orders in Extensiv Order Manager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/order`
- **Base URL:** `https://api.skubana.com`
- **Official documentation:** [Create Order](https://documentation.skubana.com/pages/order-manager.html#tag/Order/operation/putOrderUsingPUT)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amountPaid` | body | `object` | no |
| `amountPaid.amount` | body | `number` | no |
| `confirmationCost.amount` | body | `number` | no |
| `customFieldValues[].customFieldDefId` | body | `string` | no |
| `customsDeclarationItems.country` | body | `string` | no |
| `customsDeclarationItems.declaredValue.amount` | body | `number` | no |
| `customShipBilling.accountNumber` | body | `string` | no |
| `customShipBilling.codAmount.amount` | body | `number` | no |
| `discount.amount` | body | `number` | no |
| `insuranceCost.amount` | body | `number` | no |
| `insuredValue.amount` | body | `number` | no |
| `orderTotal.amount` | body | `number` | no |
| `shipMethod.ltlFtlShipment` | body | `object` | no |
| `shipMethod.ltlFtlShipment.boxCount` | body | `number` | no |
| `shipMethod.ltlFtlShipment.contact.email` | body | `string` | no |
| `shipMethod.ltlFtlShipment.pallets[].height` | body | `number` | no |
| `shipMethod.ltlFtlShipment.pallets[].packages[].height` | body | `number` | no |
| `shippingCost.amount` | body | `number` | no |
| `amountPaid.currency` | body | `string` | no |
| `billDutiesToPayor` | body | `boolean` | no |
| `confirmationCost.currency` | body | `string` | no |
| `customsDeclarationItems.declaredValue` | body | `object` | no |
| `customsDeclarationItems.declaredValue.currency` | body | `string` | no |
| `customShipBilling.billingZipCode` | body | `string` | no |
| `customShipBilling.codAmount.currency` | body | `string` | no |
| `discount.currency` | body | `string` | no |
| `insuranceCost.currency` | body | `string` | no |
| `insuredValue.currency` | body | `string` | no |
| `orderTotal.currency` | body | `string` | no |
| `shipMethod.ltlFtlShipment.contact` | body | `object` | no |
| `shipMethod.ltlFtlShipment.contact.fax` | body | `string` | no |
| `shipMethod.ltlFtlShipment.pallets[].id` | body | `number` | no |
| `shipMethod.ltlFtlShipment.pallets[].packages[].id` | body | `number` | no |
| `shipMethod.packageTypeId` | body | `number` | no |
| `shippingCost.currency` | body | `string` | no |
| `confirmationCost` | body | `object` | no |
| `customsDeclarationItems.description` | body | `string` | no |
| `customShipBilling.codAmount` | body | `object` | no |
| `shipMethod.ltlFtlShipment.contact.id` | body | `number` | no |
| `shipMethod.ltlFtlShipment.freightReadyDate` | body | `string` | no |
| `shipMethod.ltlFtlShipment.pallets[].length` | body | `number` | no |
| `shipMethod.ltlFtlShipment.pallets[].packages[].length` | body | `number` | no |
| `shipMethod.shippingCarrier` | body | `string` | no |
| `containsAlcohol` | body | `boolean` | no |
| `customsDeclarationItems.harmonizationCode` | body | `string` | no |
| `customShipBilling.country` | body | `string` | no |
| `shipMethod.ltlFtlShipment.contact.name` | body | `string` | no |
| `shipMethod.ltlFtlShipment.id` | body | `number` | no |
| `shipMethod.ltlFtlShipment.pallets[].packages[].packagingTypeId` | body | `number` | no |
| `shipMethod.ltlFtlShipment.pallets[].packagingType` | body | `string` | no |
| `shipMethod.shippingProviderId` | body | `number` | no |
| `containsDryIce` | body | `boolean` | no |
| `customsDeclarationItems.productId` | body | `number` | no |
| `shipMethod.ltlFtlShipment.contact.phone` | body | `string` | no |
| `shipMethod.ltlFtlShipment.liabilityCoverage` | body | `number` | no |
| `shipMethod.ltlFtlShipment.pallets[].packages[].width` | body | `number` | no |
| `shipMethod.ltlFtlShipment.pallets[].width` | body | `number` | no |
| `shipMethod.shippingServiceId` | body | `number` | no |
| `customField1` | body | `string` | no |
| `customsDeclarationItems.quantity` | body | `number` | no |
| `shipMethod.ltlFtlShipment.liabilityType` | body | `string` | no |
| `shipMethod.ltlFtlShipment.pallets[].packages[]` | body | `array<object>` | no |
| `customField2` | body | `string` | no |
| `customsDeclarationItems.weight` | body | `number` | no |
| `shipMethod.ltlFtlShipment.measurementUnitId` | body | `number` | no |
| `customField3` | body | `string` | no |
| `customsDeclarationItems.weightUnit` | body | `string` | no |
| `shipMethod.ltlFtlShipment.pallets[]` | body | `array<object>` | no |
| `customFieldValues[]` | body | `array<object>` | no |
| `shipMethod.ltlFtlShipment.roleType` | body | `string` | no |
| `customShipBilling` | body | `object` | no |
| `shipMethod.ltlFtlShipment.sellerDeclaredValue` | body | `number` | no |
| `customShipBillingOption` | body | `string` | no |
| `shipMethod.ltlFtlShipment.sellerFreightClass` | body | `string` | no |
| `customsDeclarationItems` | body | `object` | no |
| `shipMethod.ltlFtlShipment.specialService` | body | `string` | no |
| `customsDeclarationType` | body | `string` | no |
| `shipMethod.ltlFtlShipment.totalWeight` | body | `number` | no |
| `deliveryConfirmation` | body | `string` | no |
| `discount` | body | `object` | no |
| `doNotPrepayPostage` | body | `boolean` | no |
| `dryIceWeight` | body | `number` | no |
| `gift` | body | `boolean` | no |
| `giftMessage` | body | `string` | no |
| `height` | body | `number` | no |
| `holdUntilDate` | body | `string` | no |
| `includeReturnLabel` | body | `boolean` | no |
| `insuranceCost` | body | `object` | yes |
| `insuranceProvider` | body | `string` | no |
| `insuredValue` | body | `object` | yes |
| `internalNotes` | body | `string` | no |
| `length` | body | `number` | no |
| `nonMachinable` | body | `boolean` | no |
| `notesFromBuyer` | body | `string` | no |
| `notesToBuyer` | body | `string` | no |
| `orderDate` | body | `string` | no |
| `orderItems[]` | body | `array` | no |
| `orderNumber` | body | `string` | no |
| `orderTotal` | body | `object` | no |
| `paymentDate` | body | `string` | no |
| `receiveByDate` | body | `string` | no |
| `releaseWithoutSignature` | body | `boolean` | no |
| `requestedShippingService` | body | `string` | no |
| `salesChannelId` | body | `number` | yes |
| `saturdayDelivery` | body | `boolean` | no |
| `shipAddress1` | body | `string` | yes |
| `shipAddress2` | body | `string` | no |
| `shipAddress3` | body | `string` | no |
| `shipByDate` | body | `string` | no |
| `shipCity` | body | `string` | yes |
| `shipCompany` | body | `string` | no |
| `shipCountry` | body | `string` | yes |
| `shipEmail` | body | `string` | no |
| `shipMethod` | body | `object` | no |
| `shipName` | body | `string` | yes |
| `shipPhone` | body | `string` | no |
| `shipState` | body | `string` | no |
| `shipZipCode` | body | `string` | no |
| `shippingCost` | body | `object` | no |
| `showPostage` | body | `boolean` | no |
| `suppressChannelUpdate` | body | `boolean` | no |
| `weight` | body | `number` | no |
| `width` | body | `number` | no |
