# Auth0 Management: Create User

Creates a user in Auth0 Management API.

```
POST https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/create-user', {
  method: 'POST',
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
      "blocked": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "nickname": "Ava Chen",
      "picture": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `created_at` | date |  |
| `email` | string |  |
| `name` | string |  |
| `nickname` | string |  |
| `picture` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native Auth0 Management API, this operation is `POST /users` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

