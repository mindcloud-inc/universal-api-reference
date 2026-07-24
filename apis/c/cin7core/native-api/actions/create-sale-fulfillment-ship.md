# Create Sale Fulfillment Ship with Cin7 Core

## Endpoint

- **Method:** `POST`
- **Path:** `sale/fulfilment/ship`
- **Base URL:** `https://inventory.dearsystems.com/externalapi/v2/`
- **Official documentation:** [Create Sale Fulfillment Ship](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-ship/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Lines[].ShipmentDate` | body | `date` | no |
| `ShippingAddress.DisplayAddressLine1` | body | `string` | no |
| `Lines[].Carrier` | body | `string` | no |
| `ShippingAddress.DisplayAddressLine2` | body | `string` | no |
| `Lines[].Box` | body | `string` | no |
| `ShippingAddress.Line1` | body | `string` | no |
| `Lines[].TrackingNumber` | body | `string` | no |
| `ShippingAddress.Line2` | body | `string` | no |
| `Lines[].TrackingURL` | body | `string` | no |
| `ShippingAddress.City` | body | `string` | no |
| `Lines[].IsShipped` | body | `boolean` | no |
| `ShippingAddress.State` | body | `string` | no |
| `ShippingAddress.Postcode` | body | `string` | no |
| `ShippingAddress.Country` | body | `string` | no |
| `ShippingAddress.Company` | body | `string` | no |
| `ShippingAddress.Contact` | body | `string` | no |
| `ShippingAddress.ShipToOther` | body | `boolean` | no |
| `Lines[]` | body | `array<object>` | no |
| `RequireBy` | body | `string` | no |
| `ShippingAddress` | body | `object` | no |
| `ShippingNotes` | body | `string` | no |
| `Status` | body | `string` | yes |
| `TaskID` | body | `string` | yes |
