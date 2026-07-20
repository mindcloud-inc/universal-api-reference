# Amazon Seller: Create Shipment

Creates a merchant fulfillment shipment in Amazon Seller.

```
POST https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shippingServiceId": "string",
  "shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.stateOrProvinceCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shippingServiceId": "string",
    "shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.stateOrProvinceCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `labelFormatOption.includePackingSlipWithLabel` | boolean | no | When true, include a packing slip with the label. |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.city` | string | no |  |
| `shipmentRequestDetails.labelCustomization.customTextForLabel` | string | no | Custom text to print on the label. Note: Custom text is only included on labels that are in ZPL format (ZPL203). FedEx does not support CustomTextForLabel. |
| `shipmentRequestDetails.labelCustomization.standardIdForLabel` | string | no | The type of standard identifier to print on the label. Allowed: `AmazonOrderId` Value Description AmazonOrderId Amazon-defined order identifier in 3-7-7 format is the StandardIdForLabel. Example: `AmazonOrderId`. |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.city` | string | no |  |
| `shipmentRequestDetails.shippingServiceOptions.labelFormat` | list<string> | no | The label format. Allowed: `PDF`, `PNG`, `ZPL203`, `ZPL300`, `ShippingServiceDefault` Format,Description PDF,Portable Document Format (pdf). PNG,Portable Network Graphics (png) format. ZPL203,"Zebra Programming Language (zpl) format, 203 dots per inch resolution." ZPL300,"Zebra Programming Language (zpl) format, 300 dots per inch resolution." ShippingServiceDefault,The default provided by the shipping service. Sources https://gitee.com/llzunmin/spapi |
| `shippingServiceId` | string | yes | An Amazon-defined shipping service identifier. |
| `shippingServiceOfferId` | string | no | Identifies a shipping service order made by a carrier. |
| `shipmentRequestDetails` | object | no |  |
| `shippingServiceId` | string | no |  |
| `shippingServiceOfferId` | string | no |  |
| `hazmatType` | string | no |  |
| `labelFormatOption` | object | no |  |
| `shipmentLevelSellerInputsList[]` | array | no |  |
| `accept` | string | no |  |
| `contentType` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalInputFieldName` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput` | object | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.dataType` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress` | object | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine1` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine2` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine3` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.city` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.countryCode` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.districtOrCounty` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.email` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.name` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.phone` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.postalCode` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.stateOrProvinceCode` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsBoolean` | boolean | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsCurrency` | object | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsCurrency.amount` | number | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsCurrency.currencyCode` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsDimension` | object | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsDimension.unit` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsDimension.value` | number | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsInteger` | number | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsString` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsTimestamp` | date | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsWeight` | object | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsWeight.unit` | string | no |  |
| `shipmentLevelSellerInputsList[].additionalSellerInput.valueAsWeight.value` | number | no |  |
| `shipmentRequestDetails.amazonOrderId` | string | no |  |
| `shipmentRequestDetails.hazmatType` | string | no |  |
| `shipmentRequestDetails.itemList[]` | array | no |  |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails` | object | no |  |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails.packingGroup` | string | no |  |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails.packingInstruction` | string | no |  |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails.transportationRegulatoryClass` | string | no |  |
| `shipmentRequestDetails.itemList[].dangerousGoodsDetails.unitedNationsRegulatoryId` | string | no |  |
| `shipmentRequestDetails.itemList[].isHazmat` | boolean | no |  |
| `shipmentRequestDetails.itemList[].itemDescription` | string | no |  |
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[]` | array | no |  |
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
| `shipmentRequestDetails.itemList[].itemLevelSellerInputsList[].additionalSellerInput.valueAsAddress.stateOrProvinceCode` | string | yes |  |
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
| `shipmentRequestDetails.itemList[].itemWeight` | object | no |  |
| `shipmentRequestDetails.itemList[].itemWeight.unit` | string | no |  |
| `shipmentRequestDetails.itemList[].itemWeight.value` | number | no |  |
| `shipmentRequestDetails.itemList[].liquidVolume` | object | no |  |
| `shipmentRequestDetails.itemList[].liquidVolume.unit` | string | no |  |
| `shipmentRequestDetails.itemList[].liquidVolume.value` | number | no |  |
| `shipmentRequestDetails.itemList[].orderItemId` | string | no |  |
| `shipmentRequestDetails.itemList[].quantity` | number | no |  |
| `shipmentRequestDetails.itemList[].transparencyCodeList` | list | no |  |
| `shipmentRequestDetails.labelCustomization` | object | no |  |
| `shipmentRequestDetails.labelFormatOption` | object | no |  |
| `shipmentRequestDetails.labelFormatOption.includePackingSlipWithLabel` | boolean | no |  |
| `shipmentRequestDetails.mustArriveByDate` | date | no |  |
| `shipmentRequestDetails.packageDimensions` | object | no |  |
| `shipmentRequestDetails.packageDimensions.height` | number | no |  |
| `shipmentRequestDetails.packageDimensions.length` | number | no |  |
| `shipmentRequestDetails.packageDimensions.predefinedPackageDimensions` | string | no |  |
| `shipmentRequestDetails.packageDimensions.unit` | string | no |  |
| `shipmentRequestDetails.packageDimensions.width` | number | no |  |
| `shipmentRequestDetails.sellerOrderId` | string | no |  |
| `shipmentRequestDetails.shipDate` | date | no |  |
| `shipmentRequestDetails.shipFromAddress` | object | no |  |
| `shipmentRequestDetails.shipFromAddress.addressLine1` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.addressLine2` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.addressLine3` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.city` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.countryCode` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.districtOrCounty` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.email` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.name` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.phone` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.postalCode` | string | no |  |
| `shipmentRequestDetails.shipFromAddress.stateOrProvinceCode` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[]` | array | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalInputFieldName` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput` | object | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.dataType` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress` | object | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine1` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine2` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.addressLine3` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.countryCode` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.districtOrCounty` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.email` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.name` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.phone` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.postalCode` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsAddress.stateOrProvinceCode` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsBoolean` | boolean | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsCurrency` | object | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsCurrency.amount` | number | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsCurrency.currencyCode` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsDimension` | object | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsDimension.unit` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsDimension.value` | number | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsInteger` | number | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsString` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsTimestamp` | date | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsWeight` | object | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsWeight.unit` | string | no |  |
| `shipmentRequestDetails.shipmentLevelSellerInputsList[].additionalSellerInput.valueAsWeight.value` | number | no |  |
| `shipmentRequestDetails.shippingServiceId` | string | no |  |
| `shipmentRequestDetails.shippingServiceOfferId` | string | no |  |
| `shipmentRequestDetails.shippingServiceOptions` | object | no |  |
| `shipmentRequestDetails.shippingServiceOptions.carrierWillPickUp` | boolean | no |  |
| `shipmentRequestDetails.shippingServiceOptions.carrierWillPickUpOption` | string | no |  |
| `shipmentRequestDetails.shippingServiceOptions.declaredValue` | object | no |  |
| `shipmentRequestDetails.shippingServiceOptions.declaredValue.amount` | number | no |  |
| `shipmentRequestDetails.shippingServiceOptions.declaredValue.currencyCode` | string | no |  |
| `shipmentRequestDetails.shippingServiceOptions.deliveryExperience` | string | no |  |
| `shipmentRequestDetails.weight` | object | no |  |
| `shipmentRequestDetails.weight.unit` | string | no |  |
| `shipmentRequestDetails.weight.value` | number | no |  |

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

Through the native Amazon Seller API, this operation is `POST mfn/v0/shipments` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

