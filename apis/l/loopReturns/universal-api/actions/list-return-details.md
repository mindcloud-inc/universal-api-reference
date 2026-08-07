# Loop Returns: Get Return Details

Get the details of a specific return based on a return’s ID, an order name, or a Shopify order ID.

```
GET https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-return-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop Returns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-return-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-return-details?${params}`, {
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
| `returnID` | string | no |  |
| `orderID` | string | no |  |
| `orderName` | string | no |  |
| `currencyType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "createdAt": "string",
      "currency": "string",
      "customer": "string",
      "customerEmail": "ava@example.com",
      "customerFirstName": "Ava",
      "customerLastName": "Chen",
      "destinationId": 1,
      "editedAt": "string",
      "exchange": "string",
      "exchangeCreditTotal": "string",
      "exchangeDiscountTotal": "string",
      "exchangeProductTotal": "string",
      "exchangeTaxTotal": "string",
      "exchangeTotal": "string",
      "giftCard": "string",
      "giftCardOrderId": {},
      "giftCardOrderName": {},
      "handlingFee": "string",
      "id": 1,
      "labelRate": 1,
      "labels": [
        {
          "carrier": "string",
          "lineItems": [
            1
          ],
          "rate": 1,
          "status": "string",
          "trackingNumber": "string",
          "updatedAt": "string",
          "url": "https://example.com"
        }
      ],
      "labelStatus": "string",
      "labelUpdatedAt": "string",
      "labelUrl": "https://example.com",
      "lineItems": [
        {
          "barcode": "string",
          "condition": {},
          "consolidationTracking": {},
          "discount": "string",
          "disposition": {},
          "exchangeVariant": {},
          "image": "string",
          "lineItemId": 1,
          "lineItemTitle": "string",
          "outcome": "string",
          "parentReason": "string",
          "price": "string",
          "productId": 1,
          "providerLineItemId": 1,
          "providerRestockLocationId": {},
          "reason": "string",
          "refund": "string",
          "refundItem": "string",
          "refundTax": "string",
          "returnComment": "string",
          "returnedAt": "string",
          "sku": "string",
          "tax": "string",
          "title": "string",
          "variantId": 1,
          "variantTitle": {}
        }
      ],
      "multiCurrency": true,
      "orderId": 1,
      "orderName": "Ava Chen",
      "orderNumber": 1,
      "originCountry": "string",
      "originCountryCode": "string",
      "outcome": "string",
      "outcomesProcessedAt": {
        "exchangeProcessed": {},
        "giftCardProcessed": {},
        "refundProcessed": {},
        "returnProcessed": {}
      },
      "packageReference": "string",
      "providerOrderId": 1,
      "providerOrderNumber": 1,
      "refund": "string",
      "refundBeforeInspection": true,
      "returnCreditTotal": "string",
      "returnDiscountTotal": "string",
      "returnMethod": {},
      "returnProductTotal": "string",
      "returnTaxTotal": "string",
      "returnTotal": "string",
      "state": "string",
      "statusPageUrl": "https://example.com",
      "total": "string",
      "trackingNumber": "string",
      "type": "string",
      "updatedAt": "string",
      "upsell": "string",
      "wasProcessed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customer` | string |  |
| `customerEmail` | string |  |
| `customerFirstName` | string |  |
| `customerLastName` | string |  |
| `destinationId` | number |  |
| `editedAt` | string |  |
| `exchange` | string |  |
| `exchangeCreditTotal` | string |  |
| `exchangeDiscountTotal` | string |  |
| `exchangeProductTotal` | string |  |
| `exchangeTaxTotal` | string |  |
| `exchangeTotal` | string |  |
| `giftCard` | string |  |
| `giftCardOrderId` | object |  |
| `giftCardOrderName` | object |  |
| `handlingFee` | string |  |
| `id` | number |  |
| `labelRate` | number |  |
| `labels[].carrier` | string |  |
| `labels[].lineItems[]` | number |  |
| `labels[].rate` | number |  |
| `labels[].status` | string |  |
| `labels[].trackingNumber` | string |  |
| `labels[].updatedAt` | string |  |
| `labels[].url` | string |  |
| `labelStatus` | string |  |
| `labelUpdatedAt` | string |  |
| `labelUrl` | string |  |
| `lineItems[].barcode` | string |  |
| `lineItems[].condition` | object |  |
| `lineItems[].consolidationTracking` | object |  |
| `lineItems[].discount` | string |  |
| `lineItems[].disposition` | object |  |
| `lineItems[].exchangeVariant` | object |  |
| `lineItems[].image` | string |  |
| `lineItems[].lineItemId` | number |  |
| `lineItems[].lineItemTitle` | string |  |
| `lineItems[].outcome` | string |  |
| `lineItems[].parentReason` | string |  |
| `lineItems[].price` | string |  |
| `lineItems[].productId` | number |  |
| `lineItems[].providerLineItemId` | number |  |
| `lineItems[].providerRestockLocationId` | object |  |
| `lineItems[].reason` | string |  |
| `lineItems[].refund` | string |  |
| `lineItems[].refundItem` | string |  |
| `lineItems[].refundTax` | string |  |
| `lineItems[].returnComment` | string |  |
| `lineItems[].returnedAt` | string |  |
| `lineItems[].sku` | string |  |
| `lineItems[].tax` | string |  |
| `lineItems[].title` | string |  |
| `lineItems[].variantId` | number |  |
| `lineItems[].variantTitle` | object |  |
| `multiCurrency` | boolean |  |
| `orderId` | number |  |
| `orderName` | string |  |
| `orderNumber` | number |  |
| `originCountry` | string |  |
| `originCountryCode` | string |  |
| `outcome` | string |  |
| `outcomesProcessedAt.exchangeProcessed` | object |  |
| `outcomesProcessedAt.giftCardProcessed` | object |  |
| `outcomesProcessedAt.refundProcessed` | object |  |
| `outcomesProcessedAt.returnProcessed` | object |  |
| `packageReference` | string |  |
| `providerOrderId` | number |  |
| `providerOrderNumber` | number |  |
| `refund` | string |  |
| `refundBeforeInspection` | boolean |  |
| `returnCreditTotal` | string |  |
| `returnDiscountTotal` | string |  |
| `returnMethod` | object |  |
| `returnProductTotal` | string |  |
| `returnTaxTotal` | string |  |
| `returnTotal` | string |  |
| `state` | string |  |
| `statusPageUrl` | string |  |
| `total` | string |  |
| `trackingNumber` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `upsell` | string |  |
| `wasProcessed` | boolean |  |

## Native endpoint

Through the native Loop Returns API, this operation is `GET /warehouse/return/details` (base URL `https://api.loopreturns.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-return-details.md) for the provider-specific parameters and requirements.

