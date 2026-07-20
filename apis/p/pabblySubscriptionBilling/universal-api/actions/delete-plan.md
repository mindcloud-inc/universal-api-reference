# Pabbly Subscription Billing: Delete Plan



```
DELETE https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-plan?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "billingCycle": "string",
      "billingCycleNum": "string",
      "billingPeriod": "string",
      "billingPeriodNum": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "planActive": "string",
      "planCode": "string",
      "planDescription": "string",
      "planName": "Ava Chen",
      "price": 1,
      "productId": "string",
      "setupFee": 1,
      "trialPeriod": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingCycle` | string |  |
| `billingCycleNum` | string |  |
| `billingPeriod` | string |  |
| `billingPeriodNum` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `planActive` | string |  |
| `planCode` | string |  |
| `planDescription` | string |  |
| `planName` | string |  |
| `price` | number |  |
| `productId` | string |  |
| `setupFee` | number |  |
| `trialPeriod` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `DELETE /v1/plans/:planId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-plan.md) for the provider-specific parameters and requirements.

