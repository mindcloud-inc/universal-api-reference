# CrowdPower: Get Customer

Retrieves a customer from CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | Customer identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge_summary": {},
      "color": "string",
      "created_at": 1,
      "custom_attributes": [
        {}
      ],
      "device": {},
      "email": "ava@example.com",
      "event_summaries": [
        {}
      ],
      "first_name": "Ava",
      "gravatar": "string",
      "has_push_notifications": true,
      "id": "string",
      "initials": "string",
      "ip": "string",
      "last_messaged_at": 1,
      "last_name": "Chen",
      "link": "https://example.com",
      "location": {},
      "name": "Ava Chen",
      "notes": "string",
      "page_summaries": [
        {}
      ],
      "phone": "string",
      "product_summaries": [
        {}
      ],
      "project_id": "string",
      "segments": [
        {}
      ],
      "session": {},
      "signed_up_at": 1,
      "stripe": [
        {}
      ],
      "tags": [
        {}
      ],
      "unsub_groups": [
        {}
      ],
      "unsubscribed_at": 1,
      "unsubscribed_sms_at": 1,
      "updated_at": 1,
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charge_summary` | object |  |
| `color` | string |  |
| `created_at` | number |  |
| `custom_attributes` | array<object> |  |
| `device` | object |  |
| `email` | string |  |
| `event_summaries` | array<object> |  |
| `first_name` | string |  |
| `gravatar` | string |  |
| `has_push_notifications` | boolean |  |
| `id` | string |  |
| `initials` | string |  |
| `ip` | string |  |
| `last_messaged_at` | number |  |
| `last_name` | string |  |
| `link` | string |  |
| `location` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `page_summaries` | array<object> |  |
| `phone` | string |  |
| `product_summaries` | array<object> |  |
| `project_id` | string |  |
| `segments` | array<object> |  |
| `session` | object |  |
| `signed_up_at` | number |  |
| `stripe` | array<object> |  |
| `tags` | array<object> |  |
| `unsub_groups` | array<object> |  |
| `unsubscribed_at` | number |  |
| `unsubscribed_sms_at` | number |  |
| `updated_at` | number |  |
| `user_id` | string |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET customers/:customer_id` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

