# Create Order with Amark

## Endpoint

- **Method:** `POST`
- **Path:** `/Order/Create`
- **Base URL:** `{environment}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderNumber` | body | `string` | yes | — |
| `orderId` | body | `number` | no | — |
| `orderDate` | body | `date` | no | — |
| `shipMethod` | body | `list<string>` | yes | Accepted values: `FEDEX`, `UPS`, `USPS`, `VAULT`. |
| `shipperServiceCode` | body | `list<string>` | yes | Accepted values: `EXPSVR`, `FIRST`, `FX2D`, `INTECO`, `PRIORITY`, `TRANSFER`. |
| `isDeliveryConfirm` | body | `boolean` | no | — |
| `isSignatureConfirm` | body | `boolean` | no | — |
| `isSignatureOverride` | body | `boolean` | no | — |
| `isForcedOverride` | body | `boolean` | no | — |
| `isInsured` | body | `boolean` | no | — |
| `isRegistered` | body | `boolean` | no | — |
| `items[]` | body | `array<object>` | no | — |
| `invoiceURL` | body | `string` | no | — |
| `totalUS` | body | `number` | no | — |
| `totalShipping` | body | `number` | no | — |
| `totalTax` | body | `number` | no | — |
| `totalAdjustment` | body | `number` | no | — |
| `orderNote` | body | `string` | no | — |
| `pickPackInstruction` | body | `string` | no | — |
| `invoiceData` | body | `string` | no | — |
| `gS1Data` | body | `string` | no | — |
| `paymentMethod` | body | `string` | no | — |
| `vaultAccount` | body | `string` | no | — |
| `custodian` | body | `string` | no | — |
| `isReship` | body | `boolean` | no | — |
| `feeAmount` | body | `number` | no | — |
| `isGift` | body | `boolean` | no | — |
| `giftMessage` | body | `string` | no | — |
| `feeLabel` | body | `string` | no | — |
| `isCostco` | body | `number` | no | — |
| `labelData` | body | `string` | no | — |
| `poNumber` | body | `string` | no | — |
| `canFulfill` | body | `boolean` | no | — |
| `paidStatus` | body | `string` | no | — |
| `billingLocation` | body | `object` | yes | — |
| `shippingLocation` | body | `object` | yes | — |
| `id` | body | `number` | no | — |
| `sku` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `quantity` | body | `number` | no | — |
| `totalUS` | body | `number` | no | — |
| `harmonizedCode` | body | `string` | no | — |
| `exportCode` | body | `string` | no | — |
| `shipmentDetailDesc` | body | `string` | no | — |
| `countryManufacture` | body | `string` | no | — |
| `countryManufacture_Name` | body | `string` | no | — |
| `poLineSequenceNumber` | body | `number` | no | — |
| `costcoSKU` | body | `string` | no | — |
| `companyName` | body | `string` | no | — |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `address1` | body | `string` | no | — |
| `address2` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `postalCode` | body | `string` | no | — |
| `countryISO` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `is_residential` | body | `boolean` | no | — |
| `companyName` | body | `string` | no | — |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `address1` | body | `string` | no | — |
| `address2` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `postalCode` | body | `string` | no | — |
| `countryISO` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `is_residential` | body | `boolean` | no | — |
