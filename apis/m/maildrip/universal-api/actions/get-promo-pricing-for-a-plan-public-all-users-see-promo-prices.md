# Maildrip: Get promo pricing for a plan (public - all users see promo prices)



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-promo-pricing-for-a-plan-public-all-users-see-promo-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-promo-pricing-for-a-plan-public-all-users-see-promo-prices?connectionId=$CONNECTION_ID&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-promo-pricing-for-a-plan-public-all-users-see-promo-prices?${params}`, {
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
| `planId` | string | yes | The plan ID to get pricing for |
| `currency` | string | no | Currency for pricing |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "discountedPrice": 1,
      "discountPercentage": 1,
      "hasPromo": true,
      "originalPrice": 1,
      "plan": {},
      "promoEndsAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `discountedPrice` | number |  |
| `discountPercentage` | number |  |
| `hasPromo` | boolean |  |
| `originalPrice` | number |  |
| `plan` | object |  |
| `promoEndsAt` | date |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/promo/pricing` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-promo-pricing-for-a-plan-public-all-users-see-promo-prices.md) for the provider-specific parameters and requirements.

