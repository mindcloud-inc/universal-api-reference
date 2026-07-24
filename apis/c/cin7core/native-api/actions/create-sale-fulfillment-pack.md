# Create Sale Fulfillment Pack with Cin7 Core

## Endpoint

- **Method:** `POST`
- **Path:** `sale/fulfilment/pack`
- **Base URL:** `https://inventory.dearsystems.com/externalapi/v2/`
- **Official documentation:** [Create Sale Fulfillment Pack](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-pack/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Lines[].ProductID` | body | `string` | no |
| `Lines[].SKU` | body | `string` | no |
| `Lines[].Name` | body | `string` | no |
| `Lines[].Location` | body | `string` | no |
| `Lines[].LocationID` | body | `string` | no |
| `Lines[].Box` | body | `string` | no |
| `Lines[].Quantity` | body | `number` | no |
| `Lines[].BatchSN` | body | `string` | no |
| `Lines[].ExpiryDate` | body | `string` | no |
| `Lines[].WarrantyRegistrationNumber` | body | `string` | no |
| `Lines[]` | body | `array<object>` | no |
| `Status` | body | `string` | yes |
| `TaskID` | body | `string` | yes |
