# eBay: List Orders



```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-orders?${params}`, {
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
| `creationDateStart` | string | no |  |
| `creationDateEnd` | string | no |  |
| `lastModifiedDateStart` | string | no |  |
| `lastModifiedDateEnd` | string | no |  |
| `orderfulfillmentstatus` | list | no | **Not Started - In Progress**: specifies orders for which no shipping fulfillments have been started, plus orders for which at least one shipping fulfillment has been started but not completed. **Fulfilled - In Progress**:specifies orders for which all shipping fulfillments have been completed, plus orders for which at least one shipping fulfillment has been started but not completed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyer": {
        "buyerRegistrationAddress": {
          "contactAddress": {
            "addressLine1": "string",
            "city": "string",
            "countryCode": "string",
            "postalCode": "string",
            "stateOrProvince": "string"
          },
          "email": "ava@example.com",
          "fullName": "Ava Chen",
          "primaryPhone": {
            "phoneNumber": "string"
          }
        },
        "taxAddress": {
          "countryCode": "string",
          "postalCode": "string",
          "stateOrProvince": "string"
        },
        "username": "Ava Chen"
      },
      "cancelStatus": {
        "cancelState": "string"
      },
      "creationDate": "string",
      "ebayCollectAndRemitTax": true,
      "fulfillmentStartInstructions": [
        {
          "ebaySupportedFulfillment": true,
          "fulfillmentInstructionsType": "string",
          "maxEstimatedDeliveryDate": "string",
          "minEstimatedDeliveryDate": "string",
          "shippingStep": {
            "shippingCarrierCode": "string",
            "shippingServiceCode": "string",
            "shipTo": {
              "contactAddress": {
                "addressLine1": "string",
                "city": "string",
                "countryCode": "string",
                "postalCode": "string",
                "stateOrProvince": "string"
              },
              "email": "ava@example.com",
              "fullName": "Ava Chen"
            }
          }
        }
      ],
      "lastModifiedDate": "string",
      "lineItems": [
        {
          "deliveryCost": {
            "shippingCost": {
              "currency": "string",
              "value": "string"
            }
          },
          "ebayCollectAndRemitTaxes": [
            {
              "amount": {
                "currency": "string",
                "value": "string"
              },
              "collectionMethod": "string",
              "ebayReference": {
                "name": "Ava Chen",
                "value": "string"
              },
              "taxType": "string"
            }
          ],
          "itemLocation": {
            "countryCode": "string",
            "location": "string",
            "postalCode": "string"
          },
          "legacyItemId": "string",
          "lineItemCost": {
            "currency": "string",
            "value": "string"
          },
          "lineItemFulfillmentInstructions": {
            "guaranteedDelivery": true,
            "maxEstimatedDeliveryDate": "string",
            "minEstimatedDeliveryDate": "string"
          },
          "lineItemFulfillmentStatus": "string",
          "lineItemId": "string",
          "listingMarketplaceId": "string",
          "properties": {
            "buyerProtection": true
          },
          "purchaseMarketplaceId": "string",
          "quantity": 1,
          "soldFormat": "string",
          "title": "string",
          "total": {
            "currency": "string",
            "value": "string"
          }
        }
      ],
      "orderFulfillmentStatus": "string",
      "orderId": "string",
      "orderPaymentStatus": "string",
      "paymentSummary": {
        "payments": [
          {
            "amount": {
              "convertedFromCurrency": "string",
              "convertedFromValue": "string",
              "currency": "string",
              "value": "string"
            },
            "paymentDate": "string",
            "paymentMethod": "string",
            "paymentReferenceId": "string",
            "paymentStatus": "string"
          }
        ],
        "totalDueSeller": {
          "convertedFromCurrency": "string",
          "convertedFromValue": "string",
          "currency": "string",
          "value": "string"
        }
      },
      "pricingSummary": {
        "deliveryCost": {
          "currency": "string",
          "value": "string"
        },
        "priceSubtotal": {
          "currency": "string",
          "value": "string"
        },
        "total": {
          "currency": "string",
          "value": "string"
        }
      },
      "salesRecordReference": "string",
      "sellerId": "string",
      "totalFeeBasisAmount": {
        "currency": "string",
        "value": "string"
      },
      "totalMarketplaceFee": {
        "currency": "string",
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyer.buyerRegistrationAddress.contactAddress.addressLine1` | string |  |
| `buyer.buyerRegistrationAddress.contactAddress.city` | string |  |
| `buyer.buyerRegistrationAddress.contactAddress.countryCode` | string |  |
| `buyer.buyerRegistrationAddress.contactAddress.postalCode` | string |  |
| `buyer.buyerRegistrationAddress.contactAddress.stateOrProvince` | string |  |
| `buyer.buyerRegistrationAddress.email` | string |  |
| `buyer.buyerRegistrationAddress.fullName` | string |  |
| `buyer.buyerRegistrationAddress.primaryPhone.phoneNumber` | string |  |
| `buyer.taxAddress.countryCode` | string |  |
| `buyer.taxAddress.postalCode` | string |  |
| `buyer.taxAddress.stateOrProvince` | string |  |
| `buyer.username` | string |  |
| `cancelStatus.cancelState` | string |  |
| `creationDate` | string |  |
| `ebayCollectAndRemitTax` | boolean |  |
| `fulfillmentStartInstructions[].ebaySupportedFulfillment` | boolean |  |
| `fulfillmentStartInstructions[].fulfillmentInstructionsType` | string |  |
| `fulfillmentStartInstructions[].maxEstimatedDeliveryDate` | string |  |
| `fulfillmentStartInstructions[].minEstimatedDeliveryDate` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shippingCarrierCode` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shippingServiceCode` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shipTo.contactAddress.addressLine1` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shipTo.contactAddress.city` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shipTo.contactAddress.countryCode` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shipTo.contactAddress.postalCode` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shipTo.contactAddress.stateOrProvince` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shipTo.email` | string |  |
| `fulfillmentStartInstructions[].shippingStep.shipTo.fullName` | string |  |
| `lastModifiedDate` | string |  |
| `lineItems[].deliveryCost.shippingCost.currency` | string |  |
| `lineItems[].deliveryCost.shippingCost.value` | string |  |
| `lineItems[].ebayCollectAndRemitTaxes[].amount.currency` | string |  |
| `lineItems[].ebayCollectAndRemitTaxes[].amount.value` | string |  |
| `lineItems[].ebayCollectAndRemitTaxes[].collectionMethod` | string |  |
| `lineItems[].ebayCollectAndRemitTaxes[].ebayReference.name` | string |  |
| `lineItems[].ebayCollectAndRemitTaxes[].ebayReference.value` | string |  |
| `lineItems[].ebayCollectAndRemitTaxes[].taxType` | string |  |
| `lineItems[].itemLocation.countryCode` | string |  |
| `lineItems[].itemLocation.location` | string |  |
| `lineItems[].itemLocation.postalCode` | string |  |
| `lineItems[].legacyItemId` | string |  |
| `lineItems[].lineItemCost.currency` | string |  |
| `lineItems[].lineItemCost.value` | string |  |
| `lineItems[].lineItemFulfillmentInstructions.guaranteedDelivery` | boolean |  |
| `lineItems[].lineItemFulfillmentInstructions.maxEstimatedDeliveryDate` | string |  |
| `lineItems[].lineItemFulfillmentInstructions.minEstimatedDeliveryDate` | string |  |
| `lineItems[].lineItemFulfillmentStatus` | string |  |
| `lineItems[].lineItemId` | string |  |
| `lineItems[].listingMarketplaceId` | string |  |
| `lineItems[].properties.buyerProtection` | boolean |  |
| `lineItems[].purchaseMarketplaceId` | string |  |
| `lineItems[].quantity` | number |  |
| `lineItems[].soldFormat` | string |  |
| `lineItems[].title` | string |  |
| `lineItems[].total.currency` | string |  |
| `lineItems[].total.value` | string |  |
| `orderFulfillmentStatus` | string |  |
| `orderId` | string |  |
| `orderPaymentStatus` | string |  |
| `paymentSummary.payments[].amount.convertedFromCurrency` | string |  |
| `paymentSummary.payments[].amount.convertedFromValue` | string |  |
| `paymentSummary.payments[].amount.currency` | string |  |
| `paymentSummary.payments[].amount.value` | string |  |
| `paymentSummary.payments[].paymentDate` | string |  |
| `paymentSummary.payments[].paymentMethod` | string |  |
| `paymentSummary.payments[].paymentReferenceId` | string |  |
| `paymentSummary.payments[].paymentStatus` | string |  |
| `paymentSummary.totalDueSeller.convertedFromCurrency` | string |  |
| `paymentSummary.totalDueSeller.convertedFromValue` | string |  |
| `paymentSummary.totalDueSeller.currency` | string |  |
| `paymentSummary.totalDueSeller.value` | string |  |
| `pricingSummary.deliveryCost.currency` | string |  |
| `pricingSummary.deliveryCost.value` | string |  |
| `pricingSummary.priceSubtotal.currency` | string |  |
| `pricingSummary.priceSubtotal.value` | string |  |
| `pricingSummary.total.currency` | string |  |
| `pricingSummary.total.value` | string |  |
| `salesRecordReference` | string |  |
| `sellerId` | string |  |
| `totalFeeBasisAmount.currency` | string |  |
| `totalFeeBasisAmount.value` | string |  |
| `totalMarketplaceFee.currency` | string |  |
| `totalMarketplaceFee.value` | string |  |

## Native endpoint

Through the native eBay API, this operation is `GET sell/fulfillment/v1/order` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

