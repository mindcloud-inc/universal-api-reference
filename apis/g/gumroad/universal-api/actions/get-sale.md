# Gumroad: Get Sale

Retrieves a sale from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-sale?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-sale?${params}`, {
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
| `id` | string | yes | The sale ID. |

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
        "cancelled": true,
        "canContact": true,
        "card": {
          "type": "string",
          "visual": "string"
        },
        "chargedback": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currencySymbol": "string",
        "customFields": {},
        "daystamp": "string",
        "discoverFeeCharged": true,
        "disputed": true,
        "disputeWon": true,
        "email": "ava@example.com",
        "ended": true,
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
        "licenseDisabled": true,
        "licenseId": "string",
        "licenseKey": "string",
        "offerCode": {
          "displayedAmountOff": "string",
          "name": "Ava Chen"
        },
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
        "purchaserId": "string",
        "quantity": 1,
        "recurringCharge": true,
        "referrer": "string",
        "reviewsCount": 1,
        "sellerId": "string",
        "subscriptionDuration": "string",
        "subscriptionId": "string",
        "timestamp": "string",
        "variants": {},
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
| `sale.cancelled` | boolean |  |
| `sale.canContact` | boolean |  |
| `sale.card` | object |  |
| `sale.card.type` | string |  |
| `sale.card.visual` | string |  |
| `sale.chargedback` | boolean |  |
| `sale.createdAt` | date |  |
| `sale.currencySymbol` | string |  |
| `sale.customFields` | object |  |
| `sale.daystamp` | string |  |
| `sale.discoverFeeCharged` | boolean |  |
| `sale.disputed` | boolean |  |
| `sale.disputeWon` | boolean |  |
| `sale.email` | string |  |
| `sale.ended` | boolean |  |
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
| `sale.licenseDisabled` | boolean |  |
| `sale.licenseId` | string |  |
| `sale.licenseKey` | string |  |
| `sale.offerCode` | object |  |
| `sale.offerCode.displayedAmountOff` | string |  |
| `sale.offerCode.name` | string |  |
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
| `sale.purchaserId` | string |  |
| `sale.quantity` | number |  |
| `sale.recurringCharge` | boolean |  |
| `sale.referrer` | string |  |
| `sale.reviewsCount` | number |  |
| `sale.sellerId` | string |  |
| `sale.subscriptionDuration` | string |  |
| `sale.subscriptionId` | string |  |
| `sale.timestamp` | string |  |
| `sale.variants` | object |  |
| `sale.variantsAndQuantity` | string |  |
| `sale.zipCode` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /sales/:id` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale.md) for the provider-specific parameters and requirements.

