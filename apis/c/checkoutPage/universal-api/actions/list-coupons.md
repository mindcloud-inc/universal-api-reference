# Checkout Page: List Coupons

Retrieves coupons from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-coupons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-coupons?${params}`, {
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
| `limit` | string | no | The number of results per page. Minimum value is 1 and maximum is 100. Defaults to 20. |
| `startingAfter` | string | no | A cursor value specifying the id of a resource to start before. Retrieves items that appear after this cursor in the list. Cannot be used together with `ending_before`. |
| `endingBefore` | string | no | A cursor value specifying the id of a resource to end after. Retrieves items that appear before this cursor in the list. Cannot be used together with `starting_after`. |
| `search` | string | no | Case-insensitive search matched against coupon label and code. Returns coupons where either field contains the search term. |

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

Through the native Checkout Page API, this operation is `GET /v1/coupons/` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-coupons.md) for the provider-specific parameters and requirements.

