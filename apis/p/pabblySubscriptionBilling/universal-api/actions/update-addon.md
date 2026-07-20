# Pabbly Subscription Billing: Update Addon



```
PUT https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-addon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-addon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-addon', {
  method: 'PUT',
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
      "associatePlans": "string",
      "billingCycle": "string",
      "billingPeriod": "string",
      "categoryArray": [
        "string"
      ],
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "plansArray": "string",
      "price": 1,
      "productId": "string",
      "status": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associatePlans` | string |  |
| `billingCycle` | string |  |
| `billingPeriod` | string |  |
| `categoryArray` | array<string> |  |
| `code` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `plansArray` | string |  |
| `price` | number |  |
| `productId` | string |  |
| `status` | boolean |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `PUT /v1/addon/:addonId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-addon.md) for the provider-specific parameters and requirements.

