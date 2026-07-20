# Amazon Seller: Get Shipment ( MFN )

Retrieves a merchant fulfillment shipment from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-mfn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-mfn?connectionId=$CONNECTION_ID&shipmentIdList=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipmentIdList": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-mfn?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipmentIdList` | string | yes | The Amazon-defined shipment identifier for the shipment. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amazonOrderId": "string",
      "createdDate": "string",
      "insurance": {
        "amount": 1,
        "currencyCode": "string"
      },
      "itemList": [
        {
          "dangerousGoodsDetails": {
            "packingGroup": "string",
            "packingInstruction": "string",
            "transportationRegulatoryClass": "string",
            "unitedNationsRegulatoryId": "string"
          },
          "isHazmat": true,
          "itemDescription": "string",
          "itemLevelSellerInputsList": [
            {
              "additionalInputFieldName": "Ava Chen",
              "additionalSellerInput": {
                "dataType": "string",
                "valueAsAddress": {
                  "addressLine1": "string",
                  "addressLine2": "string",
                  "addressLine3": "string",
                  "city": "string",
                  "countryCode": "string",
                  "districtOrCounty": "string",
                  "email": "ava@example.com",
                  "name": "Ava Chen",
                  "phone": "string",
                  "postalCode": "string",
                  "stateOrProvinceCode": "string"
                },
                "valueAsBoolean": true,
                "valueAsCurrency": {
                  "amount": 1,
                  "currencyCode": "string"
                },
                "valueAsDimension": {
                  "unit": "string",
                  "value": 1
                },
                "valueAsInteger": 1,
                "valueAsString": "string",
                "valueAsTimestamp": "string",
                "valueAsWeight": {
                  "unit": "string",
                  "value": 1
                }
              }
            }
          ],
          "itemWeight": {
            "unit": "string",
            "value": 1
          },
          "liquidVolume": {
            "unit": "string",
            "value": 1
          },
          "orderItemId": "string",
          "quantity": 1,
          "transparencyCodeList": [
            "string"
          ]
        }
      ],
      "label": {
        "customTextForLabel": "string",
        "dimensions": {
          "length": 1,
          "unit": "string",
          "width": 1
        },
        "fileContents": {
          "checksum": "string",
          "contents": "string",
          "fileType": "string"
        },
        "labelFormat": "string",
        "standardIdForLabel": "string"
      },
      "lastUpdatedDate": "string",
      "packageDimensions": {
        "height": 1,
        "length": 1,
        "predefinedPackageDimensions": "string",
        "unit": "string",
        "width": 1
      },
      "sellerOrderId": "string",
      "shipFromAddress": {
        "addressLine1": "string",
        "addressLine2": "string",
        "addressLine3": "string",
        "city": "string",
        "countryCode": "string",
        "districtOrCounty": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phone": "string",
        "postalCode": "string",
        "stateOrProvinceCode": "string"
      },
      "shipmentId": "string",
      "shippingService": {
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
      },
      "shipToAddress": {
        "addressLine1": "string",
        "addressLine2": "string",
        "addressLine3": "string",
        "city": "string",
        "countryCode": "string",
        "districtOrCounty": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phone": "string",
        "postalCode": "string",
        "stateOrProvinceCode": "string"
      },
      "status": "string",
      "trackingId": "string",
      "weight": {
        "unit": "string",
        "value": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amazonOrderId` | string |  |
| `createdDate` | string |  |
| `insurance.amount` | number |  |
| `insurance.currencyCode` | string |  |
| `itemList[].dangerousGoodsDetails.packingGroup` | string |  |
| `itemList[].dangerousGoodsDetails.packingInstruction` | string |  |
| `itemList[].dangerousGoodsDetails.transportationRegulatoryClass` | string |  |
| `itemList[].dangerousGoodsDetails.unitedNationsRegulatoryId` | string |  |
| `itemList[].isHazmat` | boolean |  |
| `itemList[].itemDescription` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalInputFieldName` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.dataType` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine1` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine2` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine3` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.city` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.countryCode` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.districtOrCounty` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.email` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.name` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.phone` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.postalCode` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.stateOrProvinceCode` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsBoolean` | boolean |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsCurrency.amount` | number |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsCurrency.currencyCode` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsDimension.unit` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsDimension.value` | number |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsInteger` | number |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsString` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsTimestamp` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsWeight.unit` | string |  |
| `itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsWeight.value` | number |  |
| `itemList[].itemWeight.unit` | string |  |
| `itemList[].itemWeight.value` | number |  |
| `itemList[].liquidVolume.unit` | string |  |
| `itemList[].liquidVolume.value` | number |  |
| `itemList[].orderItemId` | string |  |
| `itemList[].quantity` | number |  |
| `itemList[].transparencyCodeList[]` | string |  |
| `label.customTextForLabel` | string |  |
| `label.dimensions.length` | number |  |
| `label.dimensions.unit` | string |  |
| `label.dimensions.width` | number |  |
| `label.fileContents.checksum` | string |  |
| `label.fileContents.contents` | string |  |
| `label.fileContents.fileType` | string |  |
| `label.labelFormat` | string |  |
| `label.standardIdForLabel` | string |  |
| `lastUpdatedDate` | string |  |
| `packageDimensions.height` | number |  |
| `packageDimensions.length` | number |  |
| `packageDimensions.predefinedPackageDimensions` | string |  |
| `packageDimensions.unit` | string |  |
| `packageDimensions.width` | number |  |
| `sellerOrderId` | string |  |
| `shipFromAddress.addressLine1` | string |  |
| `shipFromAddress.addressLine2` | string |  |
| `shipFromAddress.addressLine3` | string |  |
| `shipFromAddress.city` | string |  |
| `shipFromAddress.countryCode` | string |  |
| `shipFromAddress.districtOrCounty` | string |  |
| `shipFromAddress.email` | string |  |
| `shipFromAddress.name` | string |  |
| `shipFromAddress.phone` | string |  |
| `shipFromAddress.postalCode` | string |  |
| `shipFromAddress.stateOrProvinceCode` | string |  |
| `shipmentId` | string |  |
| `shippingService.adjustmentItemList[].rateItemCharge.amount` | number |  |
| `shippingService.adjustmentItemList[].rateItemCharge.currencyCode` | string |  |
| `shippingService.adjustmentItemList[].rateItemID` | string |  |
| `shippingService.adjustmentItemList[].rateItemNameLocalization` | string |  |
| `shippingService.adjustmentItemList[].rateItemType` | string |  |
| `shippingService.availableFormatOptionsForLabel[].includePackingSlipWithLabel` | boolean |  |
| `shippingService.availableFormatOptionsForLabel[].labelFormat` | string |  |
| `shippingService.availableLabelFormats[]` | string |  |
| `shippingService.availableShippingServiceOptions.availableCarrierWillPickUpOptions[].carrierWillPickUpOption` | string |  |
| `shippingService.availableShippingServiceOptions.availableCarrierWillPickUpOptions[].charge.amount` | number |  |
| `shippingService.availableShippingServiceOptions.availableCarrierWillPickUpOptions[].charge.currencyCode` | string |  |
| `shippingService.availableShippingServiceOptions.availableDeliveryExperienceOptions[].charge.amount` | number |  |
| `shippingService.availableShippingServiceOptions.availableDeliveryExperienceOptions[].charge.currencyCode` | string |  |
| `shippingService.availableShippingServiceOptions.availableDeliveryExperienceOptions[].deliveryExperienceOption` | string |  |
| `shippingService.benefits.excludedBenefits[].benefit` | string |  |
| `shippingService.benefits.excludedBenefits[].reasonCodes[]` | string |  |
| `shippingService.benefits.includedBenefits[]` | string |  |
| `shippingService.carrierName` | string |  |
| `shippingService.earliestEstimatedDeliveryDate` | string |  |
| `shippingService.latestEstimatedDeliveryDate` | string |  |
| `shippingService.rate.amount` | number |  |
| `shippingService.rate.currencyCode` | string |  |
| `shippingService.rateWithAdjustments.amount` | number |  |
| `shippingService.rateWithAdjustments.currencyCode` | string |  |
| `shippingService.requiresAdditionalSellerInputs` | boolean |  |
| `shippingService.shipDate` | string |  |
| `shippingService.shippingServiceId` | string |  |
| `shippingService.shippingServiceName` | string |  |
| `shippingService.shippingServiceOfferId` | string |  |
| `shippingService.shippingServiceOptions.carrierWillPickUp` | boolean |  |
| `shippingService.shippingServiceOptions.carrierWillPickUpOption` | string |  |
| `shippingService.shippingServiceOptions.declaredValue.amount` | number |  |
| `shippingService.shippingServiceOptions.declaredValue.currencyCode` | string |  |
| `shippingService.shippingServiceOptions.deliveryExperience` | string |  |
| `shippingService.shippingServiceOptions.labelFormat` | string |  |
| `shipToAddress.addressLine1` | string |  |
| `shipToAddress.addressLine2` | string |  |
| `shipToAddress.addressLine3` | string |  |
| `shipToAddress.city` | string |  |
| `shipToAddress.countryCode` | string |  |
| `shipToAddress.districtOrCounty` | string |  |
| `shipToAddress.email` | string |  |
| `shipToAddress.name` | string |  |
| `shipToAddress.phone` | string |  |
| `shipToAddress.postalCode` | string |  |
| `shipToAddress.stateOrProvinceCode` | string |  |
| `status` | string |  |
| `trackingId` | string |  |
| `weight.unit` | string |  |
| `weight.value` | number |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET mfn/v0/shipments/:shipmentId` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-mfn.md) for the provider-specific parameters and requirements.

