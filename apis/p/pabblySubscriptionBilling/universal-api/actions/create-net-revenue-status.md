# Pabbly Subscription Billing: Create Net-Revenue Status



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-net-revenue-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-net-revenue-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-net-revenue-status?${params}`, {
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
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "referenceId": "string",
      "status": "string",
      "type": "string"
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
| `emailId` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `referenceId` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/revenuetransaction` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-net-revenue-status.md) for the provider-specific parameters and requirements.

