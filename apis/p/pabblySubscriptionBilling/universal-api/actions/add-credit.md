# Pabbly Subscription Billing: Add Credit



```
POST https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/add-credit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/add-credit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/add-credit', {
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
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditNoteId": "string",
      "customerId": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "planId": "string",
      "productId": "string",
      "quantity": 1,
      "rate": 1,
      "remainingAmount": 1,
      "status": "string",
      "subscriptionId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "used": [
        "string"
      ],
      "usedDays": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdAt` | date |  |
| `creditNoteId` | string |  |
| `customerId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `planId` | string |  |
| `productId` | string |  |
| `quantity` | number |  |
| `rate` | number |  |
| `remainingAmount` | number |  |
| `status` | string |  |
| `subscriptionId` | string |  |
| `updatedAt` | date |  |
| `used` | array<string> |  |
| `usedDays` | number |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/subscription/credit/:subscriptionId/create` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-credit.md) for the provider-specific parameters and requirements.

