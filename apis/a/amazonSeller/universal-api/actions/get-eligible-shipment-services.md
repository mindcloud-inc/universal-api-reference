# Amazon Seller: Get Eligible Shipment Services

Retrieves eligible shipping service offers from Amazon Seller.

```
POST https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-eligible-shipment-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-eligible-shipment-services" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-eligible-shipment-services', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.City` | string | no |  |
| `shipmentRequestDetails.itemList[].itemWeight.unit` | string<string> | no | `oz` - the unit of weight is ounces. `g` - the unit of weight is grams. |
| `shipmentRequestDetails.shipFromAddress.City` | string | no |  |
| `shipmentRequestDetails.amazonOrderId` | string | no |  |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails.unitedNationsRegulatoryId` | string | no | The specific UNID of the item being shipped. |
| `shipmentRequestDetails.itemList[].liquidVolume.unit` | string<string> | no |  |
| `shipmentRequestDetails.itemList[].orderItemId` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.name` | string | no | The name of the addressee, or business name. |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails.transportationRegulatoryClass` | string | no | The specific regulatory class of the shipped item. |
| `shipmentRequestDetails.itemList[].liquidVolume.value` | number | no | The measurement value. |
| `shipmentRequestDetails.itemList[].quantity` | number | no |  |
| `shipmentRequestDetails.sellerOrderId` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.email` | string | no | The email address. |
| `shippingOfferingFilter` | object | no |  |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails.packingGroup` | string | no | The specific packaging group of the item being shipped. |
| `shipmentRequestDetails.itemList[].itemDescription` | string | no |  |
| `shipmentRequestDetails.shipDate` | date | no |  |
| `shipmentRequestDetails.shipFromAddress.phone` | string | no | The phone number. |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails.packingInstruction` | string | no | The specific packing instruction of the item being shipped. |
| `shipmentRequestDetails.itemList[].isHazmat` | boolean | no | When true, the item qualifies as hazardous materials (hazmat). Defaults to false. |
| `shipmentRequestDetails.mustArriveByDate` | date | no | Date-time formatted timestamp. |
| `shipmentRequestDetails.shipFromAddress.addressLine1` | string | no | The street address information. |
| `shipmentRequestDetails.itemList[]` | array<object> | no |  |
| `shipmentRequestDetails.itemList[].itemWeight` | object | no |  |
| `shipmentRequestDetails.shipFromAddress.addressLine2` | string | no | Additional street address information. |
| `shipmentRequestDetails.itemList[].transparencyCodeList` | list<string> | no | Accepts multiple values as an array. |
| `shipmentRequestDetails.shipFromAddress` | object | no | The postal address information. |
| `shipmentRequestDetails.shipFromAddress.addressLine3` | string | no | Additional street address information. |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[]` | array | no |  |
| `shipmentRequestDetails.packageDimensions` | object | no | The dimensions of a package contained in a shipment. |
| `shipmentRequestDetails.shipFromAddress.districtOrCounty` | string | no | The district or county. |
| `shipmentRequestDetails.itemList[].liquidVolume` | object | no | Liquid volume. |
| `shipmentRequestDetails.shipFromAddress.City` | string | no |  |
| `shipmentRequestDetails.weight` | object | no | The weight. |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails` | object | no | Details related to any dangerous goods or items that are shipped. |
| `shipmentRequestDetails.shipFromAddress.stateOrProvinceCode` | string | no | The state or province code. This is a required field in Canada, US, and UK marketplaces, and for shipments that originate in China. |
| `shipmentRequestDetails.shippingServiceOptions` | object | no | Extra services provided by a carrier. |
| `shipmentRequestDetails.labelCustomization` | object | no | Custom text for shipping labels. |
| `shipmentRequestDetails.shipFromAddress.postalCode` | string | no | The zip code or postal code. |
| `shipmentRequestDetails.shipFromAddress.countryCode` | string | no | The two-letter country code in `ISO 3166-1 alpha-2` format. |
| `accept` | string | no |  |
| `contentType` | string | no |  |
| `shipmentRequestDetails` | object | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalInputFieldName` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput` | object | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.dataType` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress` | object | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine1` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine2` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine3` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.countryCode` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.districtOrCounty` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.email` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.name` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.phone` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.postalCode` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.stateOrProvinceCode` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsBoolean` | boolean | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsCurrency` | object | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsCurrency.amount` | number | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsCurrency.currencyCode` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsDimension` | object | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsDimension.unit` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsDimension.value` | number | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsInteger` | number | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsString` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsTimestamp` | date | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsWeight` | object | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsWeight.unit` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsWeight.value` | number | no |  |
| `shipmentRequestDetails.itemList[].itemWeight.value` | number | no |  |
| `shipmentRequestDetails.labelCustomization.customTextForLabel` | string | no |  |
| `shipmentRequestDetails.labelCustomization.standardIdForLabel` | string | no |  |
| `shipmentRequestDetails.packageDimensions.height` | number | no |  |
| `shipmentRequestDetails.packageDimensions.length` | number | no |  |
| `shipmentRequestDetails.packageDimensions.predefinedPackageDimensions` | string | no |  |
| `shipmentRequestDetails.packageDimensions.unit` | string | no |  |
| `shipmentRequestDetails.packageDimensions.width` | number | no |  |
| `shipmentRequestDetails.shippingServiceOptions.carrierWillPickUp` | boolean | no |  |
| `shipmentRequestDetails.shippingServiceOptions.carrierWillPickUpOption` | string | no |  |
| `shipmentRequestDetails.shippingServiceOptions.declaredValue` | object | no |  |
| `shipmentRequestDetails.shippingServiceOptions.declaredValue.amount` | number | no |  |
| `shipmentRequestDetails.shippingServiceOptions.declaredValue.currencyCode` | string | no |  |
| `shipmentRequestDetails.shippingServiceOptions.deliveryExperience` | string | no |  |
| `shipmentRequestDetails.shippingServiceOptions.labelFormat` | string | no |  |
| `shipmentRequestDetails.weight.unit` | string | no |  |
| `shipmentRequestDetails.weight.value` | number | no |  |
| `shippingOfferingFilter.carrierWillPickUp` | string<string> | no |  |
| `shippingOfferingFilter.deliveryExperience` | string<string> | no |  |
| `shippingOfferingFilter.includeComplexShippingOptions` | boolean | no |  |
| `shippingOfferingFilter.includePackingSlipWithLabel` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {
          "code": "string",
          "details": "string",
          "message": "string"
        }
      ],
      "shippingServiceList": [
        {
          "adjustmentItemList": [
            {
              "rateItemCharge": {
                "amount": 1,
                "currencyCode": "string"
              },
              "rateItemID": "string",
              "rateItemNameLocalization": "Ava Chen",
              "rateItemType": "string"
            }
          ],
          "availableFormatOptionsForLabel": [
            {
              "includePackingSlipWithLabel": true,
              "labelFormat": "string"
            }
          ],
          "availableLabelFormats": [
            "string"
          ],
          "availableShippingServiceOptions": {
            "availableCarrierWillPickUpOptions": [
              {
                "carrierWillPickUpOption": "string",
                "charge": {
                  "amount": 1,
                  "currencyCode": "string"
                }
              }
            ],
            "availableDeliveryExperienceOptions": [
              {
                "charge": {
                  "amount": 1,
                  "currencyCode": "string"
                },
                "deliveryExperienceOption": "string"
              }
            ]
          },
          "benefits": {
            "excludedBenefits": [
              {
                "benefit": "string",
                "reasonCodes": [
                  "string"
                ]
              }
            ],
            "includedBenefits": [
              "string"
            ]
          },
          "carrierName": "Ava Chen",
          "earliestEstimatedDeliveryDate": "string",
          "latestEstimatedDeliveryDate": "string",
          "rate": {
            "amount": 1,
            "currencyCode": "string"
          },
          "rateWithAdjustments": {
            "amount": 1,
            "currencyCode": "string"
          },
          "requiresAdditionalSellerInputs": true,
          "shipDate": "string",
          "shippingServiceId": "string",
          "shippingServiceName": "Ava Chen",
          "shippingServiceOfferId": "string",
          "shippingServiceOptions": {
            "carrierWillPickUp": true,
            "carrierWillPickUpOption": "string",
            "declaredValue": {
              "amount": 1,
              "currencyCode": "string"
            },
            "deliveryExperience": "string",
            "labelFormat": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors[].code` | string |  |
| `errors[].details` | string |  |
| `errors[].message` | string |  |
| `shippingServiceList[].adjustmentItemList[].rateItemCharge.amount` | number |  |
| `shippingServiceList[].adjustmentItemList[].rateItemCharge.currencyCode` | string |  |
| `shippingServiceList[].adjustmentItemList[].rateItemID` | string |  |
| `shippingServiceList[].adjustmentItemList[].rateItemNameLocalization` | string |  |
| `shippingServiceList[].adjustmentItemList[].rateItemType` | string |  |
| `shippingServiceList[].availableFormatOptionsForLabel[].includePackingSlipWithLabel` | boolean |  |
| `shippingServiceList[].availableFormatOptionsForLabel[].labelFormat` | string |  |
| `shippingServiceList[].availableLabelFormats[]` | string |  |
| `shippingServiceList[].availableShippingServiceOptions.availableCarrierWillPickUpOptions[].carrierWillPickUpOption` | string |  |
| `shippingServiceList[].availableShippingServiceOptions.availableCarrierWillPickUpOptions[].charge.amount` | number |  |
| `shippingServiceList[].availableShippingServiceOptions.availableCarrierWillPickUpOptions[].charge.currencyCode` | string |  |
| `shippingServiceList[].availableShippingServiceOptions.availableDeliveryExperienceOptions[].charge.amount` | number |  |
| `shippingServiceList[].availableShippingServiceOptions.availableDeliveryExperienceOptions[].charge.currencyCode` | string |  |
| `shippingServiceList[].availableShippingServiceOptions.availableDeliveryExperienceOptions[].deliveryExperienceOption` | string |  |
| `shippingServiceList[].benefits.excludedBenefits[].benefit` | string |  |
| `shippingServiceList[].benefits.excludedBenefits[].reasonCodes[]` | string |  |
| `shippingServiceList[].benefits.includedBenefits[]` | string |  |
| `shippingServiceList[].carrierName` | string |  |
| `shippingServiceList[].earliestEstimatedDeliveryDate` | string |  |
| `shippingServiceList[].latestEstimatedDeliveryDate` | string |  |
| `shippingServiceList[].rate.amount` | number |  |
| `shippingServiceList[].rate.currencyCode` | string |  |
| `shippingServiceList[].rateWithAdjustments.amount` | number |  |
| `shippingServiceList[].rateWithAdjustments.currencyCode` | string |  |
| `shippingServiceList[].requiresAdditionalSellerInputs` | boolean |  |
| `shippingServiceList[].shipDate` | string |  |
| `shippingServiceList[].shippingServiceId` | string |  |
| `shippingServiceList[].shippingServiceName` | string |  |
| `shippingServiceList[].shippingServiceOfferId` | string |  |
| `shippingServiceList[].shippingServiceOptions.carrierWillPickUp` | boolean |  |
| `shippingServiceList[].shippingServiceOptions.carrierWillPickUpOption` | string |  |
| `shippingServiceList[].shippingServiceOptions.declaredValue.amount` | number |  |
| `shippingServiceList[].shippingServiceOptions.declaredValue.currencyCode` | string |  |
| `shippingServiceList[].shippingServiceOptions.deliveryExperience` | string |  |
| `shippingServiceList[].shippingServiceOptions.labelFormat` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `POST mfn/v0/eligibleShippingServices` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-eligible-shipment-services.md) for the provider-specific parameters and requirements.

