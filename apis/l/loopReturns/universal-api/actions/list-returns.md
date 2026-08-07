# Loop Returns: List Returns

Pull a detailed list of returns created within a given timeframe.

```
GET https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-returns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop Returns `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-returns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-returns?${params}`, {
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
| `state` | list<string> | no | Only include returns in a particular state. If left blank, the response may include __open__, __closed__, and __expired__ returns. Available options: `open`, `closed`, `cancelled`, `expired`, `review` |
| `from` | date | no |  |
| `to` | date | no |  |
| `filter` | list<string> | no | The date used to filter results. Available options: `created_at`, `updated_at` |

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
      "destinationId": 1,
      "editedAt": {},
      "exchangeCreditTotal": "string",
      "exchangeDiscountTotal": "string",
      "exchangeProductTotal": "string",
      "exchangeTaxTotal": "string",
      "exchangeTotal": "string",
      "giftCard": "string",
      "giftCardOrderId": {},
      "giftCardOrderName": {},
      "handlingFee": "string",
      "id": "string",
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
          "exchangeVariant": "string",
          "lineItemId": "string",
          "outcome": "string",
          "parentReturnReason": "string",
          "price": "string",
          "productId": "string",
          "providerLineItemId": "string",
          "providerRestockLocationId": {},
          "refund": "string",
          "refundItem": "string",
          "refundTax": "string",
          "returnComment": "string",
          "returnedAt": "string",
          "returnReason": "string",
          "sku": "string",
          "tax": "string",
          "title": "string",
          "variantId": "string"
        }
      ],
      "multiCurrency": true,
      "orderId": "string",
      "orderName": "Ava Chen",
      "orderNumber": "string",
      "originCountry": "string",
      "originCountryCode": "string",
      "outcome": "string",
      "outcomesProcessedAt": {
        "exchangeProcessed": {},
        "giftCardProcessed": {},
        "refundProcessed": {
          "date": "string",
          "timezone": "string",
          "timezoneType": 1
        },
        "returnProcessed": {
          "date": "string",
          "timezone": "string",
          "timezoneType": 1
        },
        "shopCashProcessed": {}
      },
      "packageReference": "string",
      "providerOrderId": "string",
      "providerOrderNumber": "string",
      "refund": "string",
      "refundBeforeInspection": true,
      "returnCreditTotal": "string",
      "returnDiscountTotal": "string",
      "returnMethod": {},
      "returnProductTotal": "string",
      "returnTaxTotal": "string",
      "returnTotal": "string",
      "shopifyRefundObject": [
        {
          "createdAt": "string",
          "id": 1,
          "providerCreatedAt": "string",
          "providerRefundId": 1,
          "returnId": 1,
          "updatedAt": "string"
        }
      ],
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
| `destinationId` | number |  |
| `editedAt` | object |  |
| `exchangeCreditTotal` | string |  |
| `exchangeDiscountTotal` | string |  |
| `exchangeProductTotal` | string |  |
| `exchangeTaxTotal` | string |  |
| `exchangeTotal` | string |  |
| `giftCard` | string |  |
| `giftCardOrderId` | object |  |
| `giftCardOrderName` | object |  |
| `handlingFee` | string |  |
| `id` | string |  |
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
| `lineItems[].exchangeVariant` | string |  |
| `lineItems[].lineItemId` | string |  |
| `lineItems[].outcome` | string |  |
| `lineItems[].parentReturnReason` | string |  |
| `lineItems[].price` | string |  |
| `lineItems[].productId` | string |  |
| `lineItems[].providerLineItemId` | string |  |
| `lineItems[].providerRestockLocationId` | object |  |
| `lineItems[].refund` | string |  |
| `lineItems[].refundItem` | string |  |
| `lineItems[].refundTax` | string |  |
| `lineItems[].returnComment` | string |  |
| `lineItems[].returnedAt` | string |  |
| `lineItems[].returnReason` | string |  |
| `lineItems[].sku` | string |  |
| `lineItems[].tax` | string |  |
| `lineItems[].title` | string |  |
| `lineItems[].variantId` | string |  |
| `multiCurrency` | boolean |  |
| `orderId` | string |  |
| `orderName` | string |  |
| `orderNumber` | string |  |
| `originCountry` | string |  |
| `originCountryCode` | string |  |
| `outcome` | string |  |
| `outcomesProcessedAt.exchangeProcessed` | object |  |
| `outcomesProcessedAt.giftCardProcessed` | object |  |
| `outcomesProcessedAt.refundProcessed.date` | string |  |
| `outcomesProcessedAt.refundProcessed.timezone` | string |  |
| `outcomesProcessedAt.refundProcessed.timezoneType` | number |  |
| `outcomesProcessedAt.returnProcessed.date` | string |  |
| `outcomesProcessedAt.returnProcessed.timezone` | string |  |
| `outcomesProcessedAt.returnProcessed.timezoneType` | number |  |
| `outcomesProcessedAt.shopCashProcessed` | object |  |
| `packageReference` | string |  |
| `providerOrderId` | string |  |
| `providerOrderNumber` | string |  |
| `refund` | string |  |
| `refundBeforeInspection` | boolean |  |
| `returnCreditTotal` | string |  |
| `returnDiscountTotal` | string |  |
| `returnMethod` | object |  |
| `returnProductTotal` | string |  |
| `returnTaxTotal` | string |  |
| `returnTotal` | string |  |
| `shopifyRefundObject[].createdAt` | string |  |
| `shopifyRefundObject[].id` | number |  |
| `shopifyRefundObject[].providerCreatedAt` | string |  |
| `shopifyRefundObject[].providerRefundId` | number |  |
| `shopifyRefundObject[].returnId` | number |  |
| `shopifyRefundObject[].updatedAt` | string |  |
| `state` | string |  |
| `statusPageUrl` | string |  |
| `total` | string |  |
| `trackingNumber` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `upsell` | string |  |
| `wasProcessed` | boolean |  |

## Native endpoint

Through the native Loop Returns API, this operation is `GET /warehouse/return/list` (base URL `https://api.loopreturns.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-returns.md) for the provider-specific parameters and requirements.

