# Create Sale Fulfillment Pick with Cin7 Core

## Endpoint

- **Method:** `POST`
- **Path:** `sale/fulfilment/pick`
- **Base URL:** `https://inventory.dearsystems.com/externalapi/v2/`
- **Official documentation:** [Create Sale Fulfillment Pick](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-pack/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Lines[].ProductID` | body | `string` | no |
| `Lines[].SKU` | body | `string` | no |
| `Lines[].Name` | body | `string` | no |
| `Lines[].Location` | body | `string` | no |
| `Lines[].LocationID` | body | `string` | no |
| `Lines[].Quantity` | body | `number` | no |
| `Lines[].BatchSN` | body | `string` | no |
| `Lines[].ExpiryDate` | body | `string` | no |
| `Lines[]` | body | `array<object>` | no |
| `Status` | body | `string` | yes |
| `TaskID` | body | `string` | yes |
