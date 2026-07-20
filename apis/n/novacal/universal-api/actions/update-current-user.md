# Novacal: Update Current User

Updates the current user in Novacal.

```
PUT https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-current-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-current-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Novacal API, this operation is `PUT /v1/users/me` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-current-user.md) for the provider-specific parameters and requirements.

