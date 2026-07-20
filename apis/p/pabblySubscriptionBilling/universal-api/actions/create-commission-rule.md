# Pabbly Subscription Billing: Create Commission Rule



```
POST https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-commission-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-commission-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-commission-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "firstAmount": 1,
      "firstAmountType": "string",
      "noOfTiers": 1,
      "planId": "string",
      "productId": "string",
      "rebillAmountType": "string",
      "ruleTitle": "string",
      "subscriptionOnly": true,
      "tiers": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | string |  |
| `createdAt` | date |  |
| `firstAmount` | number |  |
| `firstAmountType` | string |  |
| `noOfTiers` | number |  |
| `planId` | string |  |
| `productId` | string |  |
| `rebillAmountType` | string |  |
| `ruleTitle` | string |  |
| `subscriptionOnly` | boolean |  |
| `tiers` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/affiliate/commissionrule/create` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-commission-rule.md) for the provider-specific parameters and requirements.

