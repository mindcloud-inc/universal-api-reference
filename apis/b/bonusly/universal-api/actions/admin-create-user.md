# Bonusly: Admin Create User

Creates a new user in Bonusly.

```
POST https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/admin-create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/admin-create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/admin-create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The user's email address. |
| `firstName` | string | yes | The user's first name. |
| `lastName` | string | yes | The user's last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `POST /users` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-create-user.md) for the provider-specific parameters and requirements.

