# Yotpo Loyalty & Referrals: Adjust Customer Points Balance

Updates a customer's points balance in Yotpo Loyalty & Referrals.

```
PUT https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/adjust-customer-points-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/adjust-customer-points-balance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pointAdjustmentAmount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/adjust-customer-points-balance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pointAdjustmentAmount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerEmail` | string | no | Customer email address. Required if customerId is not provided. |
| `customerId` | string | no | Customer identifier from your system. |
| `pointAdjustmentAmount` | number | yes | Positive values add points and negative values remove points. |
| `applyAdjustmentToPointsEarned` | boolean | no | Whether the adjustment should also change the customer's total points earned value. |
| `historyTitle` | string | no | Optional override for the history description shown to the customer. |
| `visibleToCustomer` | boolean | no | Whether the manual adjustment should be visible to the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "customerId": 1,
      "id": 1,
      "merchantId": 1,
      "name": "Ava Chen",
      "referralId": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Timestamp when the point adjustment was created. |
| `customerId` | number | Yotpo customer identifier affected by the adjustment. |
| `id` | number | Unique identifier of the point adjustment event. |
| `merchantId` | number | Yotpo merchant identifier. |
| `name` | string | Adjustment event name. |
| `referralId` | number | Associated referral identifier when present. |
| `type` | string | Adjustment event type. |
| `updatedAt` | string | Timestamp when the point adjustment was last updated. |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/points/adjust` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/adjust-customer-points-balance.md) for the provider-specific parameters and requirements.

