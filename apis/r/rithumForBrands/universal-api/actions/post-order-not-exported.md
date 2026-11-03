# Rithum for Brands: Mark Order Not Exported

Mark an order as not exported.

```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/post-order-not-exported
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/post-order-not-exported?connectionId=$CONNECTION_ID&orderID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/post-order-not-exported?${params}`, {
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
| `orderID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string"
      },
      "additionalCostOrDiscount": 1,
      "billingAddressLine1": "string",
      "billingAddressLine2": "string",
      "billingCity": "string",
      "billingCompanyJobTitle": {},
      "billingCompanyName": {},
      "billingCountry": "string",
      "billingDaytimePhone": "string",
      "billingEveningPhone": "string",
      "billingFirstName": "Ava",
      "billingLastName": "Chen",
      "billingPostalCode": "string",
      "billingStateOrProvince": "string",
      "billingStateOrProvinceName": "Ava Chen",
      "billingSuffix": "string",
      "billingTitle": {},
      "buyerEmailAddress": "ava@example.com",
      "buyerEmailOptIn": true,
      "buyerUserId": "string",
      "checkoutDateUtc": "string",
      "checkoutSourceID": {},
      "checkoutStatus": "string",
      "createdDateUtc": "string",
      "currency": "string",
      "deliverByDateUtc": {},
      "distributionCenterTypeRollup": "string",
      "estimatedShipDateUtc": {},
      "flagDescription": {},
      "flagID": 1,
      "fulfillments": [
        {
          "channelReturnLabelFormat": {},
          "createdDateUtc": "string",
          "deliveryStatus": "string",
          "distributionCenterID": 1,
          "earliestDeliveryDateUtc": {},
          "earliestShipDateUtc": {},
          "estimatedDeliveryDateUtc": {},
          "estimatedShipDateUtc": {},
          "externalFulfillmentCenterCode": {},
          "externalFulfillmentNumber": {},
          "externalFulfillmentReferenceNumber": {},
          "externalFulfillmentStatus": "string",
          "hasChannelPackingSlip": true,
          "hasChannelReturnLabel": true,
          "hasReturnLabel": true,
          "hasShippingLabel": true,
          "id": 1,
          "insuranceCost": 1,
          "items": [
            {
              "distributionCenterCalculatedItemUnitCost": {},
              "distributionCenterCalculatedShippingCost": {},
              "distributionCenterItemUnitCost": {},
              "distributionCenterShippingCost": {},
              "fulfillmentID": 1,
              "id": 1,
              "marketplaceShippingStatus": "string",
              "orderID": 1,
              "orderItemID": 1,
              "productID": 1,
              "profileID": 1,
              "quantity": 1,
              "referenceProductID": {},
              "referenceSku": {},
              "sellerFulfillmentItemID": {},
              "sku": "string",
              "warehouseLocation": {}
            }
          ],
          "labelFormat": {},
          "orderID": 1,
          "profileID": 1,
          "returnLabelFormat": {},
          "returnTrackingNumber": {},
          "sellerFulfillmentID": {},
          "serialShippingContainerCode": {},
          "shippedDateUtc": {},
          "shippingCarrier": "string",
          "shippingClass": "string",
          "shippingCost": 1,
          "shippingLabelRequestID": {},
          "stagingLocation": {},
          "taxCost": 1,
          "trackingNumber": {},
          "trackingUrl": {},
          "type": "string",
          "updatedDateUtc": "string"
        }
      ],
      "giftOptionsTaxType": "string",
      "id": 1,
      "importDateUtc": "string",
      "items": [
        {
          "fulfillmentItems": [
            {
              "distributionCenterCalculatedItemUnitCost": {},
              "distributionCenterCalculatedShippingCost": {},
              "distributionCenterItemUnitCost": {},
              "distributionCenterShippingCost": {},
              "fulfillmentID": 1,
              "id": 1,
              "marketplaceShippingStatus": "string",
              "orderID": 1,
              "orderItemID": 1,
              "productID": 1,
              "profileID": 1,
              "quantity": 1,
              "referenceProductID": {},
              "referenceSku": {},
              "sellerFulfillmentItemID": {},
              "sku": "string",
              "warehouseLocation": {}
            }
          ],
          "giftMessage": {},
          "giftNotes": {},
          "giftPrice": 1,
          "giftTaxPrice": 1,
          "harmonizedCode": {},
          "id": 1,
          "isBundle": true,
          "itemURL": "https://example.com",
          "orderID": 1,
          "productID": 1,
          "profileID": 1,
          "quantity": 1,
          "recyclingFee": 1,
          "referenceProductID": {},
          "referenceSku": {},
          "sellerOrderItemID": {},
          "shippingPrice": 1,
          "shippingTaxPrice": 1,
          "siteListingID": "string",
          "siteOrderItemID": "string",
          "sku": "string",
          "taxPrice": 1,
          "title": "string",
          "unitEstimatedShippingCost": 1,
          "unitPrice": 1
        }
      ],
      "orderTags": "string",
      "orderTaxType": "string",
      "paymentCreditCardLast4": "string",
      "paymentDateUtc": "string",
      "paymentMerchantReferenceNumber": {},
      "paymentMethod": "string",
      "paymentPaypalAccountID": {},
      "paymentStatus": "string",
      "paymentTransactionID": {},
      "privateNotes": "string",
      "profileID": 1,
      "promotionAmount": 1,
      "promotionCode": {},
      "publicNotes": {},
      "requestedShippingCarrier": "string",
      "requestedShippingClass": "string",
      "resellerID": {},
      "secondarySiteOrderID": "string",
      "sellerOrderID": {},
      "shippingAddressLine1": "string",
      "shippingAddressLine2": "string",
      "shippingCity": "string",
      "shippingCompanyJobTitle": {},
      "shippingCompanyName": {},
      "shippingCountry": "string",
      "shippingDateUtc": {},
      "shippingDaytimePhone": "string",
      "shippingEveningPhone": "string",
      "shippingFirstName": "Ava",
      "shippingLastName": "Chen",
      "shippingPostalCode": "string",
      "shippingStateOrProvince": "string",
      "shippingStateOrProvinceName": "Ava Chen",
      "shippingStatus": "string",
      "shippingSuffix": {},
      "shippingTaxType": "string",
      "shippingTitle": {},
      "siteAccountID": {},
      "siteID": 1,
      "siteName": "Ava Chen",
      "siteOrderID": "string",
      "specialInstructions": "string",
      "totalGiftOptionPrice": 1,
      "totalGiftOptionTaxPrice": 1,
      "totalInsurancePrice": 1,
      "totalPrice": 1,
      "totalShippingPrice": 1,
      "totalShippingTaxPrice": 1,
      "totalTaxPrice": 1,
      "updatedDateUtc": "string",
      "userDataPresent": 1,
      "userDataRemovalDateUTC": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string |  |
| `additionalCostOrDiscount` | number |  |
| `billingAddressLine1` | string |  |
| `billingAddressLine2` | string |  |
| `billingCity` | string |  |
| `billingCompanyJobTitle` | object |  |
| `billingCompanyName` | object |  |
| `billingCountry` | string |  |
| `billingDaytimePhone` | string |  |
| `billingEveningPhone` | string |  |
| `billingFirstName` | string |  |
| `billingLastName` | string |  |
| `billingPostalCode` | string |  |
| `billingStateOrProvince` | string |  |
| `billingStateOrProvinceName` | string |  |
| `billingSuffix` | string |  |
| `billingTitle` | object |  |
| `buyerEmailAddress` | string |  |
| `buyerEmailOptIn` | boolean |  |
| `buyerUserId` | string |  |
| `checkoutDateUtc` | string |  |
| `checkoutSourceID` | object |  |
| `checkoutStatus` | string |  |
| `createdDateUtc` | string |  |
| `currency` | string |  |
| `deliverByDateUtc` | object |  |
| `distributionCenterTypeRollup` | string |  |
| `estimatedShipDateUtc` | object |  |
| `flagDescription` | object |  |
| `flagID` | number |  |
| `fulfillments[].channelReturnLabelFormat` | object |  |
| `fulfillments[].createdDateUtc` | string |  |
| `fulfillments[].deliveryStatus` | string |  |
| `fulfillments[].distributionCenterID` | number |  |
| `fulfillments[].earliestDeliveryDateUtc` | object |  |
| `fulfillments[].earliestShipDateUtc` | object |  |
| `fulfillments[].estimatedDeliveryDateUtc` | object |  |
| `fulfillments[].estimatedShipDateUtc` | object |  |
| `fulfillments[].externalFulfillmentCenterCode` | object |  |
| `fulfillments[].externalFulfillmentNumber` | object |  |
| `fulfillments[].externalFulfillmentReferenceNumber` | object |  |
| `fulfillments[].externalFulfillmentStatus` | string |  |
| `fulfillments[].hasChannelPackingSlip` | boolean |  |
| `fulfillments[].hasChannelReturnLabel` | boolean |  |
| `fulfillments[].hasReturnLabel` | boolean |  |
| `fulfillments[].hasShippingLabel` | boolean |  |
| `fulfillments[].id` | number |  |
| `fulfillments[].insuranceCost` | number |  |
| `fulfillments[].items[].distributionCenterCalculatedItemUnitCost` | object |  |
| `fulfillments[].items[].distributionCenterCalculatedShippingCost` | object |  |
| `fulfillments[].items[].distributionCenterItemUnitCost` | object |  |
| `fulfillments[].items[].distributionCenterShippingCost` | object |  |
| `fulfillments[].items[].fulfillmentID` | number |  |
| `fulfillments[].items[].id` | number |  |
| `fulfillments[].items[].marketplaceShippingStatus` | string |  |
| `fulfillments[].items[].orderID` | number |  |
| `fulfillments[].items[].orderItemID` | number |  |
| `fulfillments[].items[].productID` | number |  |
| `fulfillments[].items[].profileID` | number |  |
| `fulfillments[].items[].quantity` | number |  |
| `fulfillments[].items[].referenceProductID` | object |  |
| `fulfillments[].items[].referenceSku` | object |  |
| `fulfillments[].items[].sellerFulfillmentItemID` | object |  |
| `fulfillments[].items[].sku` | string |  |
| `fulfillments[].items[].warehouseLocation` | object |  |
| `fulfillments[].labelFormat` | object |  |
| `fulfillments[].orderID` | number |  |
| `fulfillments[].profileID` | number |  |
| `fulfillments[].returnLabelFormat` | object |  |
| `fulfillments[].returnTrackingNumber` | object |  |
| `fulfillments[].sellerFulfillmentID` | object |  |
| `fulfillments[].serialShippingContainerCode` | object |  |
| `fulfillments[].shippedDateUtc` | object |  |
| `fulfillments[].shippingCarrier` | string |  |
| `fulfillments[].shippingClass` | string |  |
| `fulfillments[].shippingCost` | number |  |
| `fulfillments[].shippingLabelRequestID` | object |  |
| `fulfillments[].stagingLocation` | object |  |
| `fulfillments[].taxCost` | number |  |
| `fulfillments[].trackingNumber` | object |  |
| `fulfillments[].trackingUrl` | object |  |
| `fulfillments[].type` | string |  |
| `fulfillments[].updatedDateUtc` | string |  |
| `giftOptionsTaxType` | string |  |
| `id` | number |  |
| `importDateUtc` | string |  |
| `items[].fulfillmentItems[].distributionCenterCalculatedItemUnitCost` | object |  |
| `items[].fulfillmentItems[].distributionCenterCalculatedShippingCost` | object |  |
| `items[].fulfillmentItems[].distributionCenterItemUnitCost` | object |  |
| `items[].fulfillmentItems[].distributionCenterShippingCost` | object |  |
| `items[].fulfillmentItems[].fulfillmentID` | number |  |
| `items[].fulfillmentItems[].id` | number |  |
| `items[].fulfillmentItems[].marketplaceShippingStatus` | string |  |
| `items[].fulfillmentItems[].orderID` | number |  |
| `items[].fulfillmentItems[].orderItemID` | number |  |
| `items[].fulfillmentItems[].productID` | number |  |
| `items[].fulfillmentItems[].profileID` | number |  |
| `items[].fulfillmentItems[].quantity` | number |  |
| `items[].fulfillmentItems[].referenceProductID` | object |  |
| `items[].fulfillmentItems[].referenceSku` | object |  |
| `items[].fulfillmentItems[].sellerFulfillmentItemID` | object |  |
| `items[].fulfillmentItems[].sku` | string |  |
| `items[].fulfillmentItems[].warehouseLocation` | object |  |
| `items[].giftMessage` | object |  |
| `items[].giftNotes` | object |  |
| `items[].giftPrice` | number |  |
| `items[].giftTaxPrice` | number |  |
| `items[].harmonizedCode` | object |  |
| `items[].id` | number |  |
| `items[].isBundle` | boolean |  |
| `items[].itemURL` | string |  |
| `items[].orderID` | number |  |
| `items[].productID` | number |  |
| `items[].profileID` | number |  |
| `items[].quantity` | number |  |
| `items[].recyclingFee` | number |  |
| `items[].referenceProductID` | object |  |
| `items[].referenceSku` | object |  |
| `items[].sellerOrderItemID` | object |  |
| `items[].shippingPrice` | number |  |
| `items[].shippingTaxPrice` | number |  |
| `items[].siteListingID` | string |  |
| `items[].siteOrderItemID` | string |  |
| `items[].sku` | string |  |
| `items[].taxPrice` | number |  |
| `items[].title` | string |  |
| `items[].unitEstimatedShippingCost` | number |  |
| `items[].unitPrice` | number |  |
| `orderTags` | string |  |
| `orderTaxType` | string |  |
| `paymentCreditCardLast4` | string |  |
| `paymentDateUtc` | string |  |
| `paymentMerchantReferenceNumber` | object |  |
| `paymentMethod` | string |  |
| `paymentPaypalAccountID` | object |  |
| `paymentStatus` | string |  |
| `paymentTransactionID` | object |  |
| `privateNotes` | string |  |
| `profileID` | number |  |
| `promotionAmount` | number |  |
| `promotionCode` | object |  |
| `publicNotes` | object |  |
| `requestedShippingCarrier` | string |  |
| `requestedShippingClass` | string |  |
| `resellerID` | object |  |
| `secondarySiteOrderID` | string |  |
| `sellerOrderID` | object |  |
| `shippingAddressLine1` | string |  |
| `shippingAddressLine2` | string |  |
| `shippingCity` | string |  |
| `shippingCompanyJobTitle` | object |  |
| `shippingCompanyName` | object |  |
| `shippingCountry` | string |  |
| `shippingDateUtc` | object |  |
| `shippingDaytimePhone` | string |  |
| `shippingEveningPhone` | string |  |
| `shippingFirstName` | string |  |
| `shippingLastName` | string |  |
| `shippingPostalCode` | string |  |
| `shippingStateOrProvince` | string |  |
| `shippingStateOrProvinceName` | string |  |
| `shippingStatus` | string |  |
| `shippingSuffix` | object |  |
| `shippingTaxType` | string |  |
| `shippingTitle` | object |  |
| `siteAccountID` | object |  |
| `siteID` | number |  |
| `siteName` | string |  |
| `siteOrderID` | string |  |
| `specialInstructions` | string |  |
| `totalGiftOptionPrice` | number |  |
| `totalGiftOptionTaxPrice` | number |  |
| `totalInsurancePrice` | number |  |
| `totalPrice` | number |  |
| `totalShippingPrice` | number |  |
| `totalShippingTaxPrice` | number |  |
| `totalTaxPrice` | number |  |
| `updatedDateUtc` | string |  |
| `userDataPresent` | number |  |
| `userDataRemovalDateUTC` | object |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `DELETE Orders(:orderID)/Export` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-order-not-exported.md) for the provider-specific parameters and requirements.

