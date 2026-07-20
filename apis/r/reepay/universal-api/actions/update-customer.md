# Reepay: Update Customer

Updates an existing customer in Reepay.

```
PUT https://connect.mindcloud.co/v1/universal/reepay/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reepay/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `handle` | string | yes | Customer handle from Reepay. |

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
      "email": "ava@example.com",
      "failed_amount": 1,
      "failed_invoices": 1,
      "first_name": "Ava",
      "handle": "string",
      "last_name": "Chen",
      "pending_amount": 1,
      "pending_invoices": 1,
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
| `email` | string |  |
| `failed_amount` | number |  |
| `failed_invoices` | number |  |
| `first_name` | string |  |
| `handle` | string |  |
| `last_name` | string |  |
| `pending_amount` | number |  |
| `pending_invoices` | number |  |
| `refunded_amount` | number |  |
| `settled_amount` | number |  |
| `settled_invoices` | number |  |
| `subscriptions` | number |  |
| `test` | boolean |  |

## Native endpoint

Through the native Reepay API, this operation is `PUT /v1/customer/:handle` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

