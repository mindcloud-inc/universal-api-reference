# Reepay: List Customers

Retrieves customers from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-customers?${params}`, {
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
      "active_subscriptions": 1,
      "cancelled_amount": 1,
      "cancelled_invoices": 1,
      "cancelled_subscriptions": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "failed_amount": 1,
      "failed_invoices": 1,
      "handle": "string",
      "pending_amount": 1,
      "pending_invoices": 1,
      "phone": "string",
      "refunded_amount": 1,
      "settled_amount": 1,
      "settled_invoices": 1,
      "subscriptions": 1,
      "test": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_subscriptions` | number |  |
| `cancelled_amount` | number |  |
| `cancelled_invoices` | number |  |
| `cancelled_subscriptions` | number |  |
| `created` | date |  |
| `failed_amount` | number |  |
| `failed_invoices` | number |  |
| `handle` | string |  |
| `pending_amount` | number |  |
| `pending_invoices` | number |  |
| `phone` | string |  |
| `refunded_amount` | number |  |
| `settled_amount` | number |  |
| `settled_invoices` | number |  |
| `subscriptions` | number |  |
| `test` | boolean |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/list/customer` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

