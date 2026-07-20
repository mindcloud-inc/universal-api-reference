# Create Shipment with Amazon Seller

Creates a merchant fulfillment shipment in Amazon Seller.

## Endpoint

- **Method:** `POST`
- **Path:** `mfn/v0/shipments`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Create Shipment](https://developer-docs.amazon.com/sp-api/reference/getorders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LabelFormatOption.IncludePackingSlipWithLabel` | body | `boolean` | no | When true, include a packing slip with the label. |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.City` | body | `string` | no | — |
| `ShipmentRequestDetails.LabelCustomization.CustomTextForLabel` | body | `string` | no | Custom text to print on the label. Note: Custom text is only included on labels that are in ZPL format (ZPL203). FedEx does not support CustomTextForLabel. |
| `ShipmentRequestDetails.LabelCustomization.StandardIdForLabel` | body | `string` | no | The type of standard identifier to print on the label.  Allowed: `AmazonOrderId`  Value                     Description AmazonOrderId  Amazon-defined order identifier in 3-7-7 format is the StandardIdForLabel. |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.City` | body | `string` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.LabelFormat` | body | `list<string>` | no | The label format.  Allowed: `PDF`, `PNG`, `ZPL203`, `ZPL300`, `ShippingServiceDefault`  Format,Description PDF,Portable Document Format (pdf). PNG,Portable Network Graphics (png) format. ZPL203,"Zebra Programming Language (zpl) format, 203 dots per inch resolution." ZPL300,"Zebra Programming Language (zpl) format, 300 dots per inch resolution." ShippingServiceDefault,The default provided by the shipping service.  Sources https://gitee.com/llzunmin/spapi |
| `ShippingServiceId` | body | `string` | yes | An Amazon-defined shipping service identifier. |
| `shippingServiceOfferId` | body | `string` | no | Identifies a shipping service order made by a carrier. |
| `ShipmentRequestDetails` | body | `object` | no | — |
| `ShippingServiceId` | body | `string` | no | — |
| `ShippingServiceOfferId` | body | `string` | no | — |
| `HazmatType` | body | `string` | no | — |
| `LabelFormatOption` | body | `object` | no | — |
| `ShipmentLevelSellerInputsList[]` | body | `array` | no | — |
| `accept` | header | `string` | no | — |
| `content-type` | header | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalInputFieldName` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput` | body | `object` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.DataType` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress` | body | `object` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine1` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine2` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine3` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.City` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.CountryCode` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.DistrictOrCounty` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Email` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Name` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Phone` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.PostalCode` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.StateOrProvinceCode` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsBoolean` | body | `boolean` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency` | body | `object` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency.Amount` | body | `number` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency.CurrencyCode` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension` | body | `object` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension.unit` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension.value` | body | `number` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsInteger` | body | `number` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsString` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsTimestamp` | body | `date` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight` | body | `object` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight.Unit` | body | `string` | no | — |
| `ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight.Value` | body | `number` | no | — |
| `ShipmentRequestDetails.AmazonOrderId` | body | `string` | no | — |
| `ShipmentRequestDetails.HazmatType` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[]` | body | `array` | no | — |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails.PackingGroup` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails.PackingInstruction` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails.TransportationRegulatoryClass` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails.UnitedNationsRegulatoryId` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].IsHazmat` | body | `boolean` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemDescription` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[]` | body | `array` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalInputFieldName` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.DataType` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine1` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine2` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine3` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.CountryCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.DistrictOrCounty` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Email` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Name` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Phone` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.PostalCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.StateOrProvinceCode` | body | `string` | yes | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsBoolean` | body | `boolean` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency.Amount` | body | `number` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency.CurrencyCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension.unit` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension.value` | body | `number` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsInteger` | body | `number` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsString` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsTimestamp` | body | `date` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight.Unit` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight.Value` | body | `number` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemWeight` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemWeight.Unit` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemWeight.Value` | body | `number` | no | — |
| `ShipmentRequestDetails.ItemList[].LiquidVolume` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].LiquidVolume.Unit` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].LiquidVolume.Value` | body | `number` | no | — |
| `ShipmentRequestDetails.ItemList[].OrderItemId` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].Quantity` | body | `number` | no | — |
| `ShipmentRequestDetails.ItemList[].TransparencyCodeList` | body | `list` | no | — |
| `ShipmentRequestDetails.LabelCustomization` | body | `object` | no | — |
| `ShipmentRequestDetails.LabelFormatOption` | body | `object` | no | — |
| `ShipmentRequestDetails.LabelFormatOption.IncludePackingSlipWithLabel` | body | `boolean` | no | — |
| `ShipmentRequestDetails.MustArriveByDate` | body | `date` | no | — |
| `ShipmentRequestDetails.PackageDimensions` | body | `object` | no | — |
| `ShipmentRequestDetails.PackageDimensions.Height` | body | `number` | no | — |
| `ShipmentRequestDetails.PackageDimensions.Length` | body | `number` | no | — |
| `ShipmentRequestDetails.PackageDimensions.PredefinedPackageDimensions` | body | `string` | no | — |
| `ShipmentRequestDetails.PackageDimensions.Unit` | body | `string` | no | — |
| `ShipmentRequestDetails.PackageDimensions.Width` | body | `number` | no | — |
| `ShipmentRequestDetails.SellerOrderId` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipDate` | body | `date` | no | — |
| `ShipmentRequestDetails.ShipFromAddress` | body | `object` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.AddressLine1` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.AddressLine2` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.AddressLine3` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.City` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.CountryCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.DistrictOrCounty` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.Email` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.Name` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.Phone` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.PostalCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.StateOrProvinceCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[]` | body | `array` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalInputFieldName` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput` | body | `object` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.DataType` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress` | body | `object` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine1` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine2` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.AddressLine3` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.CountryCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.DistrictOrCounty` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Email` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Name` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.Phone` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.PostalCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.StateOrProvinceCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsBoolean` | body | `boolean` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency` | body | `object` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency.Amount` | body | `number` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsCurrency.CurrencyCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension` | body | `object` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension.unit` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsDimension.value` | body | `number` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsInteger` | body | `number` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsString` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsTimestamp` | body | `date` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight` | body | `object` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight.Unit` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipmentLevelSellerInputsList[].AdditionalSellerInput.ValueAsWeight.Value` | body | `number` | no | — |
| `ShipmentRequestDetails.ShippingServiceId` | body | `string` | no | — |
| `ShipmentRequestDetails.ShippingServiceOfferId` | body | `string` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions` | body | `object` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.CarrierWillPickUp` | body | `boolean` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.CarrierWillPickUpOption` | body | `string` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.DeclaredValue` | body | `object` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.DeclaredValue.Amount` | body | `number` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.DeclaredValue.CurrencyCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.DeliveryExperience` | body | `string` | no | — |
| `ShipmentRequestDetails.Weight` | body | `object` | no | — |
| `ShipmentRequestDetails.Weight.Unit` | body | `string` | no | — |
| `ShipmentRequestDetails.Weight.Value` | body | `number` | no | — |
