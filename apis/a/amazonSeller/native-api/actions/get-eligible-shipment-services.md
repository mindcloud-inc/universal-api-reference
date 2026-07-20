# Get Eligible Shipment Services with Amazon Seller

Retrieves eligible shipping service offers from Amazon Seller.

## Endpoint

- **Method:** `POST`
- **Path:** `mfn/v0/eligibleShippingServices`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Eligible Shipment Services](https://developer-docs.amazon.com/sp-api/reference/getorders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.City` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemWeight.Unit` | body | `string<string>` | no | `oz` - the unit of weight is ounces. `g` - the unit of weight is grams. |
| `ShipmentRequestDetails.ShipFromAddress.City` | body | `string` | no | — |
| `ShipmentRequestDetails.AmazonOrderId` | body | `string` | no | — |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails.UnitedNationsRegulatoryId` | body | `string` | no | The specific UNID of the item being shipped. |
| `ShipmentRequestDetails.ItemList[].LiquidVolume.Unit` | body | `string<string>` | no | — |
| `ShipmentRequestDetails.ItemList[].OrderItemId` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.Name` | body | `string` | no | The name of the addressee, or business name. |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails.TransportationRegulatoryClass` | body | `string` | no | The specific regulatory class of the shipped item. |
| `ShipmentRequestDetails.ItemList[].LiquidVolume.Value` | body | `number` | no | The measurement value. |
| `ShipmentRequestDetails.ItemList[].Quantity` | body | `number` | no | — |
| `ShipmentRequestDetails.SellerOrderId` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.Email` | body | `string` | no | The email address. |
| `ShippingOfferingFilter` | body | `object` | no | — |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails.PackingGroup` | body | `string` | no | The specific packaging group of the item being shipped. |
| `ShipmentRequestDetails.ItemList[].ItemDescription` | body | `string` | no | — |
| `ShipmentRequestDetails.ShipDate` | body | `date` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.Phone` | body | `string` | no | The phone number. |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails.PackingInstruction` | body | `string` | no | The specific packing instruction of the item being shipped. |
| `ShipmentRequestDetails.ItemList[].IsHazmat` | body | `boolean` | no | When true, the item qualifies as hazardous materials (hazmat). Defaults to false. |
| `ShipmentRequestDetails.MustArriveByDate` | body | `date` | no | Date-time formatted timestamp. |
| `ShipmentRequestDetails.ShipFromAddress.AddressLine1` | body | `string` | no | The street address information. |
| `ShipmentRequestDetails.ItemList[]` | body | `array<object>` | no | — |
| `ShipmentRequestDetails.ItemList[].ItemWeight` | body | `object` | no | — |
| `ShipmentRequestDetails.ShipFromAddress.AddressLine2` | body | `string` | no | Additional street address information. |
| `ShipmentRequestDetails.ItemList[].TransparencyCodeList` | body | `list<string>` | no | Send multiple values as a array. |
| `ShipmentRequestDetails.ShipFromAddress` | body | `object` | no | The postal address information. |
| `ShipmentRequestDetails.ShipFromAddress.AddressLine3` | body | `string` | no | Additional street address information. |
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[]` | body | `array` | no | — |
| `ShipmentRequestDetails.PackageDimensions` | body | `object` | no | The dimensions of a package contained in a shipment. |
| `ShipmentRequestDetails.ShipFromAddress.DistrictOrCounty` | body | `string` | no | The district or county. |
| `ShipmentRequestDetails.ItemList[].LiquidVolume` | body | `object` | no | Liquid volume. |
| `ShipmentRequestDetails.ShipFromAddress.city` | body | `string` | no | — |
| `ShipmentRequestDetails.Weight` | body | `object` | no | The weight. |
| `ShipmentRequestDetails.ItemList[].DangerousGoodsDetails` | body | `object` | no | Details related to any dangerous goods or items that are shipped. |
| `ShipmentRequestDetails.ShipFromAddress.StateOrProvinceCode` | body | `string` | no | The state or province code. This is a required field in Canada, US, and UK marketplaces, and for shipments that originate in China. |
| `ShipmentRequestDetails.ShippingServiceOptions` | body | `object` | no | Extra services provided by a carrier. |
| `ShipmentRequestDetails.LabelCustomization` | body | `object` | no | Custom text for shipping labels. |
| `ShipmentRequestDetails.ShipFromAddress.PostalCode` | body | `string` | no | The zip code or postal code. |
| `ShipmentRequestDetails.ShipFromAddress.CountryCode` | body | `string` | no | The two-letter country code in `ISO 3166-1 alpha-2` format. |
| `accept` | header | `string` | no | — |
| `content-type` | header | `string` | no | — |
| `ShipmentRequestDetails` | body | `object` | no | — |
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
| `ShipmentRequestDetails.ItemList[].ItemLevelSellerInputsList[].AdditionalSellerInput.ValueAsAddress.StateOrProvinceCode` | body | `string` | no | — |
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
| `ShipmentRequestDetails.ItemList[].ItemWeight.Value` | body | `number` | no | — |
| `ShipmentRequestDetails.LabelCustomization.CustomTextForLabel` | body | `string` | no | — |
| `ShipmentRequestDetails.LabelCustomization.StandardIdForLabel` | body | `string` | no | — |
| `ShipmentRequestDetails.PackageDimensions.Height` | body | `number` | no | — |
| `ShipmentRequestDetails.PackageDimensions.Length` | body | `number` | no | — |
| `ShipmentRequestDetails.PackageDimensions.PredefinedPackageDimensions` | body | `string` | no | — |
| `ShipmentRequestDetails.PackageDimensions.Unit` | body | `string` | no | — |
| `ShipmentRequestDetails.PackageDimensions.Width` | body | `number` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.CarrierWillPickUp` | body | `boolean` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.CarrierWillPickUpOption` | body | `string` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.DeclaredValue` | body | `object` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.DeclaredValue.Amount` | body | `number` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.DeclaredValue.CurrencyCode` | body | `string` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.DeliveryExperience` | body | `string` | no | — |
| `ShipmentRequestDetails.ShippingServiceOptions.LabelFormat` | body | `string` | no | — |
| `ShipmentRequestDetails.Weight.Unit` | body | `string` | no | — |
| `ShipmentRequestDetails.Weight.Value` | body | `number` | no | — |
| `ShippingOfferingFilter.CarrierWillPickUp` | body | `string<string>` | no | — |
| `ShippingOfferingFilter.DeliveryExperience` | body | `string<string>` | no | — |
| `ShippingOfferingFilter.IncludeComplexShippingOptions` | body | `boolean` | no | — |
| `ShippingOfferingFilter.IncludePackingSlipWithLabel` | body | `boolean` | no | — |
