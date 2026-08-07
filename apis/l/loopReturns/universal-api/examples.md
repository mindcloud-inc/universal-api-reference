# Loop Returns Universal API Examples

These examples use the MindCloud API key and Loop Returns connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Returns

Pull a detailed list of returns created within a given timeframe.

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

Example response:

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

See the full [List Returns action reference](actions/list-returns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loopReturns/latest/actions/list-returns).

## Flag Return

Flag a return in Loop for review.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/flag-return" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "return_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/flag-return', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "return_id": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "errors": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Flag Return action reference](actions/flag-return.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loopReturns/latest/actions/flag-return).
