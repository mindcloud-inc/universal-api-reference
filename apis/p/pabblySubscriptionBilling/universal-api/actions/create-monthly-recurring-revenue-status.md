# Pabbly Subscription Billing: Create Monthly Recurring Revenue Status



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-monthly-recurring-revenue-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-monthly-recurring-revenue-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-monthly-recurring-revenue-status?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "status": "string",
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `emailId` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `status` | string |  |
| `totalAmount` | number |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/mrrsubscription` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-monthly-recurring-revenue-status.md) for the provider-specific parameters and requirements.

