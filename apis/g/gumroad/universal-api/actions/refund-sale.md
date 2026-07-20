# Gumroad: Refund Sale

Refunds a sale in Gumroad.

```
PUT https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/refund-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/refund-sale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/refund-sale', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The sale ID. |
| `amountCents` | number | no | Issue a partial refund for this amount in cents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sale": {
        "affiliate": {
          "amount": "string",
          "email": "ava@example.com"
        },
        "amountRefundableInCurrency": "string",
        "averageRating": 1,
        "canContact": true,
        "card": {
          "type": "string",
          "visual": "string"
        },
        "chargedback": true,
        "city": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currencySymbol": "string",
        "customFields": {},
        "daystamp": "string",
        "discoverFeeCharged": true,
        "disputed": true,
        "disputeWon": true,
        "email": "ava@example.com",
        "formattedDisplayPrice": "string",
        "formattedTotalPrice": "string",
        "gumroadFee": 1,
        "hasCustomFields": true,
        "hasVariants": true,
        "id": "string",
        "isAdditionalContribution": true,
        "isFollowing": true,
        "isGiftReceiverPurchase": true,
        "isGiftSenderPurchase": true,
        "isProductPhysical": true,
        "isRecurringBilling": true,
        "orderId": 1,
        "paid": true,
        "partiallyRefunded": true,
        "price": 1,
        "productHasVariants": true,
        "productId": "string",
        "productName": "Ava Chen",
        "productPermalink": "https://example.com",
        "productRating": 1,
        "purchaseEmail": "ava@example.com",
        "quantity": 1,
        "referrer": "string",
        "refunded": true,
        "reviewsCount": 1,
        "sellerId": "string",
        "state": "string",
        "streetAddress": "string",
        "timestamp": "string",
        "variantsAndQuantity": "string",
        "zipCode": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sale` | object |  |
| `sale.affiliate` | object |  |
| `sale.affiliate.amount` | string |  |
| `sale.affiliate.email` | string |  |
| `sale.amountRefundableInCurrency` | string |  |
| `sale.averageRating` | number |  |
| `sale.canContact` | boolean |  |
| `sale.card` | object |  |
| `sale.card.type` | string |  |
| `sale.card.visual` | string |  |
| `sale.chargedback` | boolean |  |
| `sale.city` | string |  |
| `sale.createdAt` | date |  |
| `sale.currencySymbol` | string |  |
| `sale.customFields` | object |  |
| `sale.daystamp` | string |  |
| `sale.discoverFeeCharged` | boolean |  |
| `sale.disputed` | boolean |  |
| `sale.disputeWon` | boolean |  |
| `sale.email` | string |  |
| `sale.formattedDisplayPrice` | string |  |
| `sale.formattedTotalPrice` | string |  |
| `sale.gumroadFee` | number |  |
| `sale.hasCustomFields` | boolean |  |
| `sale.hasVariants` | boolean |  |
| `sale.id` | string |  |
| `sale.isAdditionalContribution` | boolean |  |
| `sale.isFollowing` | boolean |  |
| `sale.isGiftReceiverPurchase` | boolean |  |
| `sale.isGiftSenderPurchase` | boolean |  |
| `sale.isProductPhysical` | boolean |  |
| `sale.isRecurringBilling` | boolean |  |
| `sale.orderId` | number |  |
| `sale.paid` | boolean |  |
| `sale.partiallyRefunded` | boolean |  |
| `sale.price` | number |  |
| `sale.productHasVariants` | boolean |  |
| `sale.productId` | string |  |
| `sale.productName` | string |  |
| `sale.productPermalink` | string |  |
| `sale.productRating` | number |  |
| `sale.purchaseEmail` | string |  |
| `sale.quantity` | number |  |
| `sale.referrer` | string |  |
| `sale.refunded` | boolean |  |
| `sale.reviewsCount` | number |  |
| `sale.sellerId` | string |  |
| `sale.state` | string |  |
| `sale.streetAddress` | string |  |
| `sale.timestamp` | string |  |
| `sale.variantsAndQuantity` | string |  |
| `sale.zipCode` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `PUT /sales/:id/refund` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-sale.md) for the provider-specific parameters and requirements.

