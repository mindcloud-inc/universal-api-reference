# Create/Update Shipment with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Shipment`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create/Update Shipment](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `CustomerID.value` | body | `string` | no |
| `Description.value` | body | `string` | no |
| `Details[].Allocations[].InventoryID.value` | body | `string` | no |
| `Details[].Allocations[].LocationID` | body | `object` | no |
| `Details[].Allocations[].LocationID.value` | body | `string` | no |
| `Details[].Allocations[].LotSerialNbr.value` | body | `string` | no |
| `Details[].Allocations[].Qty.value` | body | `number` | no |
| `Details[].Allocations[].UsrLPNbr.value` | body | `string` | no |
| `Details[].LocationID.value` | body | `string` | no |
| `Details[].LotSerialNbr.value` | body | `string` | no |
| `Details[].OrderLineNbr` | body | `object` | no |
| `Details[].OrderLineNbr.value` | body | `number` | no |
| `Details[].OrderNbr.value` | body | `string` | no |
| `Details[].OrderType.value` | body | `string` | no |
| `Details[].ShippedQty.value` | body | `number` | no |
| `Details[].UsrLPNbr.value` | body | `string` | no |
| `FreightCost.value` | body | `string` | no |
| `FreightPrice.value` | body | `string` | no |
| `Hold.value` | body | `boolean` | no |
| `LocationID.value` | body | `string` | no |
| `Note.value` | body | `string` | no |
| `Operation.value` | body | `string` | no |
| `Packages[].BoxID` | body | `object` | no |
| `Packages[].BoxID.value` | body | `string` | no |
| `Packages[].Description.value` | body | `string` | no |
| `Packages[].Height.value` | body | `number` | no |
| `Packages[].Length.value` | body | `number` | no |
| `Packages[].TrackingNbr.value` | body | `string` | no |
| `Packages[].Type.value` | body | `string` | no |
| `Packages[].Weight.value` | body | `number` | no |
| `Packages[].Width.value` | body | `number` | no |
| `ResidentialDelivery.value` | body | `boolean` | no |
| `ShipmentDate.value` | body | `string` | no |
| `ShippedVolume.value` | body | `number` | no |
| `ShippedWeight.value` | body | `number` | no |
| `ShippingSettings.AddressLine1.value` | body | `string` | no |
| `ShippingSettings.AddressLine2.value` | body | `string` | no |
| `ShippingSettings.Attention.value` | body | `string` | no |
| `ShippingSettings.BusinessName.value` | body | `string` | no |
| `ShippingSettings.City.value` | body | `string` | no |
| `ShippingSettings.Country.value` | body | `string` | no |
| `ShippingSettings.Email.value` | body | `string` | no |
| `ShippingSettings.Phone1.value` | body | `string` | no |
| `ShippingSettings.PostalCode.value` | body | `string` | no |
| `ShippingSettings.ShipToAddressOverride.value` | body | `boolean` | no |
| `ShippingSettings.ShipToContactOverride` | body | `object` | no |
| `ShippingSettings.ShipToContactOverride.value` | body | `boolean` | no |
| `ShippingSettings.State.value` | body | `string` | no |
| `ShipVia.value` | body | `string` | no |
| `Type.value` | body | `string` | no |
| `UsrCarrier.value` | body | `string` | no |
| `UsrDriverName.value` | body | `string` | no |
| `UsrLogiwaConf.value` | body | `boolean` | no |
| `UsrServiceLevel.value` | body | `string` | no |
| `UsrServiceLvl.value` | body | `string` | no |
| `UsrStop.value` | body | `number` | no |
| `WarehouseID.value` | body | `string` | no |
| `Details[].Allocations[].LotSerialNbr` | body | `object` | no |
| `Details[].ShippedQty` | body | `object` | no |
| `Packages[].Description` | body | `object` | no |
| `ShippingSettings.BusinessName` | body | `object` | no |
| `Type` | body | `object` | no |
| `Details[].Allocations[].Qty` | body | `object` | no |
| `Details[].OrderNbr` | body | `object` | no |
| `Hold` | body | `object` | no |
| `Packages[].TrackingNbr` | body | `object` | no |
| `ShippingSettings.Attention` | body | `object` | no |
| `Details[].Allocations[].UsrLPNbr` | body | `object` | no |
| `Details[].OrderType` | body | `object` | no |
| `Operation` | body | `object` | no |
| `Packages[].Type` | body | `object` | no |
| `ShippingSettings.Phone1` | body | `object` | no |
| `CustomerID` | body | `object` | no |
| `Details[].Allocations[].InventoryID` | body | `object` | no |
| `Details[].LotSerialNbr` | body | `object` | no |
| `Packages[].Weight` | body | `object` | no |
| `ShippingSettings.Email` | body | `object` | no |
| `Details[].LocationID` | body | `object` | no |
| `LocationID` | body | `object` | no |
| `Packages[].Length` | body | `object` | no |
| `ShippingSettings.ShipToAddressOverride` | body | `object` | no |
| `Details[].UsrLPNbr` | body | `object` | no |
| `Packages[].Width` | body | `object` | no |
| `ShipmentDate` | body | `object` | no |
| `ShippingSettings.AddressLine1` | body | `object` | no |
| `Details[].Allocations[]` | body | `array` | no |
| `Packages[].Height` | body | `object` | no |
| `ShippingSettings.AddressLine2` | body | `object` | no |
| `WarehouseID` | body | `object` | no |
| `ShippingSettings.City` | body | `object` | no |
| `UsrDriverName` | body | `object` | no |
| `ShippingSettings.State` | body | `object` | no |
| `UsrStop` | body | `object` | no |
| `ShippingSettings.PostalCode` | body | `object` | no |
| `UsrLogiwaConf` | body | `object` | no |
| `Description` | body | `object` | no |
| `ShippingSettings.Country` | body | `object` | no |
| `FreightCost` | body | `object` | no |
| `FreightPrice` | body | `object` | no |
| `ResidentialDelivery` | body | `object` | no |
| `ShipVia` | body | `object` | no |
| `ShippedWeight` | body | `object` | no |
| `ShippedVolume` | body | `object` | no |
| `Note` | body | `object` | no |
| `UsrCarrier` | body | `object` | no |
| `UsrServiceLevel` | body | `object` | no |
| `ShippingSettings` | body | `object` | no |
| `Details[]` | body | `array` | no |
| `Packages[]` | body | `array` | no |
| `UsrServiceLvl` | body | `object` | no |
