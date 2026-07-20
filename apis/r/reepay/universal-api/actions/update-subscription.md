# Reepay: Update Subscription

Updates an existing subscription in Reepay.

```
PUT https://connect.mindcloud.co/v1/universal/reepay/latest/actions/update-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/update-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reepay/latest/actions/update-subscription', {
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
| `handle` | string | yes | Subscription handle from Reepay. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activated": "2026-05-07T12:00:00.000Z",
      "cancelled_amount": 1,
      "cancelled_date": "2026-05-07T12:00:00.000Z",
      "cancelled_invoices": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "current_period_start": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "expires": "2026-05-07T12:00:00.000Z",
      "failed_amount": 1,
      "failed_invoices": 1,
      "first_period_start": "2026-05-07T12:00:00.000Z",
      "grace_duration": 1,
      "handle": "string",
      "has_started": true,
      "hosted_page_links": {
        "payment_info": "https://example.com"
      },
      "in_trial": true,
      "is_cancelled": true,
      "next_period_start": "2026-05-07T12:00:00.000Z",
      "payment_method_added": true,
      "pending_amount": 1,
      "pending_change": {
        "created": "2026-05-07T12:00:00.000Z",
        "pending": true,
        "quantity": 1
      },
      "pending_invoices": 1,
      "plan": "string",
      "plan_version": 1,
      "quantity": 1,
      "refunded_amount": 1,
      "renewal_count": 1,
      "renewing": true,
      "settled_amount": 1,
      "settled_invoices": 1,
      "start_date": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "test": true,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated` | date |  |
| `cancelled_amount` | number |  |
| `cancelled_date` | date |  |
| `cancelled_invoices` | number |  |
| `created` | date |  |
| `currency` | string |  |
| `current_period_start` | date |  |
| `customer` | string |  |
| `expires` | date |  |
| `failed_amount` | number |  |
| `failed_invoices` | number |  |
| `first_period_start` | date |  |
| `grace_duration` | number |  |
| `handle` | string |  |
| `has_started` | boolean |  |
| `hosted_page_links.payment_info` | string |  |
| `in_trial` | boolean |  |
| `is_cancelled` | boolean |  |
| `next_period_start` | date |  |
| `payment_method_added` | boolean |  |
| `pending_amount` | number |  |
| `pending_change.created` | date |  |
| `pending_change.pending` | boolean |  |
| `pending_change.quantity` | number |  |
| `pending_invoices` | number |  |
| `plan` | string |  |
| `plan_version` | number |  |
| `quantity` | number |  |
| `refunded_amount` | number |  |
| `renewal_count` | number |  |
| `renewing` | boolean |  |
| `settled_amount` | number |  |
| `settled_invoices` | number |  |
| `start_date` | date |  |
| `state` | string |  |
| `test` | boolean |  |
| `timezone` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `PUT /v1/subscription/:handle` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription.md) for the provider-specific parameters and requirements.

