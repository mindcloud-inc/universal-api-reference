# Update Sale Fulfillment Ship with Cin7 Core

## Endpoint

- **Method:** `PUT`
- **Path:** `sale/fulfilment/ship`
- **Base URL:** `https://inventory.dearsystems.com/externalapi/v2/`
- **Official documentation:** [Update Sale Fulfillment Ship](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-ship/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Lines[].ShipmentDate` | body | `string` | no |
| `ShippingAddress.DisplayAddressLine1` | body | `string` | no |
| `TaskID` | body | `string` | yes |
| `Lines[].Carrier` | body | `string` | no |
| `ShippingAddress.DisplayAddressLine2` | body | `string` | no |
| `Status` | body | `string` | yes |
| `Lines[].Box` | body | `string` | no |
| `RequireBy` | body | `string` | no |
| `ShippingAddress.Line1` | body | `string` | no |
| `Lines[].TrackingNumber` | body | `string` | no |
| `ShippingAddress` | body | `object` | no |
| `ShippingAddress.Line2` | body | `string` | no |
| `Lines[].TrackingURL` | body | `string` | no |
| `ShippingAddress.City` | body | `string` | no |
| `ShippingNotes` | body | `string` | no |
| `Lines[]` | body | `array<object>` | no |
| `Lines[].IsShipped` | body | `boolean` | no |
| `ShippingAddress.State` | body | `string` | no |
| `ShippingAddress.Postcode` | body | `string` | no |
| `ShippingAddress.Country` | body | `string` | no |
| `ShippingAddress.Company` | body | `string` | no |
| `ShippingAddress.Contact` | body | `string` | no |
| `ShippingAddress.ShipToOther` | body | `boolean` | no |
