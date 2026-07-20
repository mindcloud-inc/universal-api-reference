# CrowdPower: Get Customers

Retrieves customers from CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customers?${params}`, {
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
| `q` | string | no | Search query for customers. |

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
      "first_name": "Ava",
      "has_push_notifications": true,
      "id": "string",
      "initials": "string",
      "last_name": "Chen",
      "link": "https://example.com",
      "location": {},
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "project_id": "string",
      "session": {},
      "stripe": [
        {}
      ],
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
| `first_name` | string |  |
| `has_push_notifications` | boolean |  |
| `id` | string |  |
| `initials` | string |  |
| `last_name` | string |  |
| `link` | string |  |
| `location` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `project_id` | string |  |
| `session` | object |  |
| `stripe` | array<object> |  |
| `updated_at` | number |  |
| `user_id` | string |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET projects/{{credentials.projectId}}/customers` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customers.md) for the provider-specific parameters and requirements.

