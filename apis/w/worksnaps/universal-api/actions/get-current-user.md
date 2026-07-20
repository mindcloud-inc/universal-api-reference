# Worksnaps: Get Current User

Retrieves the current user from Worksnaps.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-current-user?${params}`, {
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
      "api_token": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "is_in_daylight_time": true,
      "last_name": "Chen",
      "login": "string",
      "timezone_id": 1,
      "timezone_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_token` | string | The current user's API token. |
| `email` | string | The user's email address. |
| `first_name` | string | The user's first name. |
| `id` | number | The Worksnaps user ID. |
| `is_in_daylight_time` | boolean | Whether daylight saving time is active. |
| `last_name` | string | The user's last name. |
| `login` | string | The Worksnaps login username. |
| `timezone_id` | number | The timezone ID. |
| `timezone_name` | string | The timezone display name. |

## Native endpoint

Through the native Worksnaps API, this operation is `GET /me.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

