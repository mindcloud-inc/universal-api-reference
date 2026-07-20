# Reepay: List Subscriptions

Retrieves subscriptions from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-subscriptions?${params}`, {
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
      "activated": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "current_period_start": "2026-05-07T12:00:00.000Z",
      "customer": "string",
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
      "renewal_count": 1,
      "renewing": true,
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
| `created` | date |  |
| `currency` | string |  |
| `current_period_start` | date |  |
| `customer` | string |  |
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
| `renewal_count` | number |  |
| `renewing` | boolean |  |
| `start_date` | date |  |
| `state` | string |  |
| `test` | boolean |  |
| `timezone` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/list/subscription` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

