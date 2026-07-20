# Checkout Page: Create Coupon

Creates a coupon in Checkout Page.

```
POST https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string",
  "code": "string",
  "duration": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-coupon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string",
    "code": "string",
    "duration": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | Internal name for the coupon. |
| `code` | string | yes | The coupon code a customer enters. |
| `amountOff` | number | no | A positive integer representing the amount to subtract from an invoice total (required if `percentOff` is not passed). |
| `currency` | string | no | Three-letter ISO code for the currency of the amountOff parameter (required if `amountOff` is passed). |
| `duration` | string | yes |  |
| `durationInMonths` | number | no | A positive integer representing the number of months the coupon applies for (required if `duration === repeating`) |
| `percentOff` | number | no | A positive float larger than 0, and smaller or equal to 100, that represents the discount the coupon will apply (required if `amountOff` is not passed). |
| `appliesToSetupFee` | boolean | no | When enabled, applies this coupon discount to the setup fee. |
| `pageIds[]` | array<string> | no | A list of pageIds that this coupon can be used within. |
| `ticketTypeIds[]` | array<string> | no | List of ticket type IDs that this coupon can be used with. Ticket ticket ids must belong to a page specified in the `pageIds` array. |
| `maxRedemptions` | number | no | The total amount of times this coupon can be used. Doesn't limit a single customer from redeeming multiple times. |
| `redeemBy` | date | no | The ISO datetime that this coupon must be used before. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountOff": 1,
      "appliesToSetupFee": true,
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "deleted": true,
      "duration": "string",
      "durationInMonths": 1,
      "id": "string",
      "label": "string",
      "maxRedemptions": 1,
      "pageIds": [
        "string"
      ],
      "percentOff": 1,
      "redeemBy": "2026-05-07T12:00:00.000Z",
      "sellerId": "string",
      "stripeCouponId": "string",
      "ticketTypeIds": [
        "string"
      ],
      "timesRedeemed": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountOff` | number | Flat discount amount in the specified `currency`. Only set if `percentOff` is not used. |
| `appliesToSetupFee` | boolean | When enabled, applies this coupon discount to the setup fee. |
| `code` | string | The coupon code a customer enters. |
| `createdAt` | date |  |
| `currency` | string | Three-letter ISO code for the `currency` (required when `amountOff` is set). Examples: usd, eur, gbp. |
| `deleted` | boolean | If true, this coupon will be soft deleted. It is no longer usable but data is retained. |
| `duration` | string | How long the discount applies: once (single payment), repeating (specified months), or forever (all future payments). |
| `durationInMonths` | number | If `duration` is `repeating`, the number of months the coupon applies. Null if coupon `duration` is forever or once. |
| `id` | string | Unique identifier for the object. |
| `label` | string | Internal name for the coupon. |
| `maxRedemptions` | number | Maximum number of times this coupon can be redeemed globally. A single customer may redeem it multiple times. |
| `pageIds` | array<string> |  |
| `percentOff` | number | Percentage discount (0-100) applied to payments using this coupon. Example: 50 applies 50% off ($100 payment becomes $50). Only set if `amountOff` is not used. |
| `redeemBy` | date | The ISO datetime that this coupon must be used before. |
| `sellerId` | string |  |
| `stripeCouponId` | string | The unique identifier of the stripe coupon that was created with this coupon. |
| `ticketTypeIds` | array<string> | List of ticket type IDs that this coupon can be used with. |
| `timesRedeemed` | number | The number of times this coupon has been redeemed. |
| `updatedAt` | date |  |

## Native endpoint

Through the native Checkout Page API, this operation is `POST /v1/coupons/` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-coupon.md) for the provider-specific parameters and requirements.

