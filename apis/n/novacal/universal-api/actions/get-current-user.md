# Novacal: Get Current User

Retrieves the current user from Novacal.

```
GET https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-current-user?${params}`, {
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
      "avatar": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "name": "Ava Chen",
      "start_of_week": 1,
      "time_format": "string",
      "timezone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | Avatar URL. |
| `email` | string | User email address. |
| `first_name` | string | First name. |
| `id` | number | User ID. |
| `last_name` | string | Last name. |
| `name` | string | Display name. |
| `start_of_week` | number | Start of week day number. |
| `time_format` | string | Preferred time format. |
| `timezone` | string | User timezone. |
| `username` | string | Novacal username. |

## Native endpoint

Through the native Novacal API, this operation is `GET /v1/users/me` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

