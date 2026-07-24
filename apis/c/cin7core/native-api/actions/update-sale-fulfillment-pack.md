# Update Sale Fulfillment Pack with Cin7 Core

## Endpoint

- **Method:** `PUT`
- **Path:** `sale/fulfilment/pack`
- **Base URL:** `https://inventory.dearsystems.com/externalapi/v2/`
- **Official documentation:** [Update Sale Fulfillment Pack](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-pack/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Lines[].ProductID` | body | `string` | no |
| `TaskID` | body | `string` | yes |
| `Lines[].SKU` | body | `string` | no |
| `Status` | body | `string` | yes |
| `Lines[]` | body | `array<object>` | no |
| `Lines[].Name` | body | `string` | no |
| `Lines[].Location` | body | `string` | no |
| `Lines[].LocationID` | body | `string` | no |
| `Lines[].Box` | body | `string` | no |
| `Lines[].Quantity` | body | `number` | no |
| `Lines[].BatchSN` | body | `string` | no |
| `Lines[].ExpiryDate` | body | `string` | no |
| `Lines[].WarrantyRegistrationNumber` | body | `string` | no |
