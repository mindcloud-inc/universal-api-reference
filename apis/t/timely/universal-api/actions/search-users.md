# Timely: Search Users

Finds users in Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/search-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/search-users?connectionId=$CONNECTION_ID&accountId=1&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/search-users?${params}`, {
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
| `accountId` | number | yes | Workspace id |
| `q` | string | yes | Search query |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "active_projects_count": 1,
      "admin": true,
      "avatar": {
        "large": "string",
        "large_retina": "string",
        "medium": "string",
        "medium_retina": "string",
        "small": "string",
        "small_retina": "string"
      },
      "created_at": 1,
      "day_view_onboarded": true,
      "default_hour_rate": 1,
      "deleted": true,
      "email": "ava@example.com",
      "external_id": "string",
      "hide_hourly_rate": true,
      "hide_internal_hourly_rate": true,
      "id": 1,
      "internal_hour_rate": 1,
      "last_received_memories_date": "string",
      "memory_onboarded": true,
      "memory_retention_days": "string",
      "name": "Ava Chen",
      "role": {
        "id": 1,
        "name": "Ava Chen"
      },
      "role_id": 1,
      "sign_in_count": "string",
      "time_zone": "string",
      "type": "string",
      "updated_at": 1,
      "user_level": "string",
      "weekdays": "string",
      "weekly_capacity": 1,
      "work_days": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `active_projects_count` | number |  |
| `admin` | boolean |  |
| `avatar` | object |  |
| `avatar.large` | string |  |
| `avatar.large_retina` | string |  |
| `avatar.medium` | string |  |
| `avatar.medium_retina` | string |  |
| `avatar.small` | string |  |
| `avatar.small_retina` | string |  |
| `created_at` | number |  |
| `day_view_onboarded` | boolean |  |
| `default_hour_rate` | number |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `external_id` | string |  |
| `hide_hourly_rate` | boolean |  |
| `hide_internal_hourly_rate` | boolean |  |
| `id` | number |  |
| `internal_hour_rate` | number |  |
| `last_received_memories_date` | string |  |
| `memory_onboarded` | boolean |  |
| `memory_retention_days` | string |  |
| `name` | string |  |
| `role` | object |  |
| `role_id` | number |  |
| `role.id` | number |  |
| `role.name` | string |  |
| `sign_in_count` | string |  |
| `time_zone` | string |  |
| `type` | string |  |
| `updated_at` | number |  |
| `user_level` | string |  |
| `weekdays` | string |  |
| `weekly_capacity` | number |  |
| `work_days` | string |  |

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/users/search` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-users.md) for the provider-specific parameters and requirements.

