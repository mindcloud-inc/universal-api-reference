# Gumroad: List Sales

Retrieves sales from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-sales?${params}`, {
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
| `after` | date | no | Only return sales after this date (YYYY-MM-DD). |
| `before` | date | no | Only return sales before this date (YYYY-MM-DD). |
| `productId` | string | no | Filter sales by this product. |
| `email` | string | no | Filter sales by this email. |
| `orderId` | number | no | Filter sales by this order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageKey": "string",
      "nextPageUrl": "https://example.com",
      "sales": [
        [
          {}
        ]
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageKey` | string |  |
| `nextPageUrl` | string |  |
| `sales[]` | array<object> |  |
| `sales[].affiliate` | object |  |
| `sales[].affiliate.amount` | string |  |
| `sales[].affiliate.email` | string |  |
| `sales[].amountRefundableInCurrency` | string |  |
| `sales[].averageRating` | number |  |
| `sales[].cancelled` | boolean |  |
| `sales[].canContact` | boolean |  |
| `sales[].card` | object |  |
| `sales[].card.type` | string |  |
| `sales[].card.visual` | string |  |
| `sales[].chargedback` | boolean |  |
| `sales[].createdAt` | date |  |
| `sales[].currencySymbol` | string |  |
| `sales[].customFields` | object |  |
| `sales[].daystamp` | string |  |
| `sales[].discoverFeeCharged` | boolean |  |
| `sales[].disputed` | boolean |  |
| `sales[].disputeWon` | boolean |  |
| `sales[].email` | string |  |
| `sales[].ended` | boolean |  |
| `sales[].formattedDisplayPrice` | string |  |
| `sales[].formattedTotalPrice` | string |  |
| `sales[].gumroadFee` | number |  |
| `sales[].hasCustomFields` | boolean |  |
| `sales[].hasVariants` | boolean |  |
| `sales[].id` | string |  |
| `sales[].isAdditionalContribution` | boolean |  |
| `sales[].isFollowing` | boolean |  |
| `sales[].isGiftReceiverPurchase` | boolean |  |
| `sales[].isGiftSenderPurchase` | boolean |  |
| `sales[].isProductPhysical` | boolean |  |
| `sales[].isRecurringBilling` | boolean |  |
| `sales[].licenseDisabled` | boolean |  |
| `sales[].licenseId` | string |  |
| `sales[].licenseKey` | string |  |
| `sales[].orderId` | number |  |
| `sales[].paid` | boolean |  |
| `sales[].partiallyRefunded` | boolean |  |
| `sales[].price` | number |  |
| `sales[].productHasVariants` | boolean |  |
| `sales[].productId` | string |  |
| `sales[].productName` | string |  |
| `sales[].productPermalink` | string |  |
| `sales[].productRating` | number |  |
| `sales[].purchaseEmail` | string |  |
| `sales[].purchaserId` | string |  |
| `sales[].quantity` | number |  |
| `sales[].recurringCharge` | boolean |  |
| `sales[].referrer` | string |  |
| `sales[].reviewsCount` | number |  |
| `sales[].sellerId` | string |  |
| `sales[].subscriptionDuration` | string |  |
| `sales[].subscriptionId` | string |  |
| `sales[].timestamp` | string |  |
| `sales[].variants` | object |  |
| `sales[].variantsAndQuantity` | string |  |
| `sales[].zipCode` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /sales` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

