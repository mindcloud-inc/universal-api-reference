# Paystack: List Subscriptions



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-subscriptions?${params}`, {
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
      "cron_expression": "string",
      "customer": {},
      "email_token": "ava@example.com",
      "id": 1,
      "next_payment_date": "string",
      "open_invoice": {},
      "plan": {},
      "status": "string",
      "subscription_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `cron_expression` | string |  |
| `customer` | object |  |
| `email_token` | string |  |
| `id` | number |  |
| `next_payment_date` | string |  |
| `open_invoice` | object |  |
| `plan` | object |  |
| `status` | string |  |
| `subscription_code` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /subscription` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

