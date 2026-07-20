# Yotpo Loyalty & Referrals: Set or Update Customer Anniversary

Updates a customer's anniversary in Yotpo Loyalty & Referrals.

```
PUT https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/set-or-update-customer-anniversary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/set-or-update-customer-anniversary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerEmail": "ava@example.com",
  "day": 1,
  "month": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/set-or-update-customer-anniversary', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerEmail": "ava@example.com",
    "day": 1,
    "month": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerEmail` | string | yes | The customer's email address. |
| `day` | number | yes | The day of the month for the anniversary. |
| `month` | number | yes | The month of the year for the anniversary. |
| `year` | number | no | The optional year for the anniversary. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yotpo Loyalty & Referrals API returns.

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/customer_anniversary` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-or-update-customer-anniversary.md) for the provider-specific parameters and requirements.

