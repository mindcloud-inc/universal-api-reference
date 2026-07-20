# Paystack: List Plans



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-plans?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-plans?${params}`, {
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
      "createdAt": "string",
      "currency": "string",
      "hosted_page": true,
      "id": 1,
      "interval": "string",
      "invoice_limit": 1,
      "is_archived": true,
      "name": "Ava Chen",
      "plan_code": "string",
      "send_invoices": true,
      "send_sms": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `hosted_page` | boolean |  |
| `id` | number |  |
| `interval` | string |  |
| `invoice_limit` | number |  |
| `is_archived` | boolean |  |
| `name` | string |  |
| `plan_code` | string |  |
| `send_invoices` | boolean |  |
| `send_sms` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /plan` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

