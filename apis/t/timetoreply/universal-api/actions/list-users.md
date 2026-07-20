# Timetoreply: List Users



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-users?${params}`, {
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
| `search` | string | no | Filter users by a search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "agent_count": 1,
      "company": "string",
      "company_id": 1,
      "complete_name": "Ava Chen",
      "confirmed": true,
      "country_code": "string",
      "created_at": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "hubspot_id": "string",
      "id": 1,
      "is_primary_user": true,
      "last_login_at": "string",
      "last_login_ip": "string",
      "lastname": "Chen",
      "phone": "string",
      "phone_confirmation_code": "string",
      "phone_confirmed": true,
      "php_time_zone": "string",
      "provider": "string",
      "provider_id": "string",
      "role": "string",
      "search_string": "string",
      "timezone": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `agent_count` | number |  |
| `company` | string |  |
| `company_id` | number |  |
| `complete_name` | string |  |
| `confirmed` | boolean |  |
| `country_code` | string |  |
| `created_at` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `hubspot_id` | string |  |
| `id` | number |  |
| `is_primary_user` | boolean |  |
| `last_login_at` | string |  |
| `last_login_ip` | string |  |
| `lastname` | string |  |
| `phone` | string |  |
| `phone_confirmation_code` | string |  |
| `phone_confirmed` | boolean |  |
| `php_time_zone` | string |  |
| `provider` | string |  |
| `provider_id` | string |  |
| `role` | string |  |
| `search_string` | string |  |
| `timezone` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/entities/users` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

