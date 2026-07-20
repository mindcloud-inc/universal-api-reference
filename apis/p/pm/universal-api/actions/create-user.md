# 5pm: Create User

Creates a new user in 5pm.

```
POST https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user.firstName": "Ava",
  "user.securityLevel": "string",
  "user.email": "ava@example.com",
  "user.password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user.firstName": "Ava",
    "user.securityLevel": "string",
    "user.email": "ava@example.com",
    "user.password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user.firstName` | string | yes | First name of the user to create. |
| `user.securityLevel` | string | yes |  |
| `user.email` | string | yes |  |
| `user.password` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "securityLevel": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | User company name. |
| `email` | string | User email address. |
| `firstName` | string | User first name. |
| `id` | string | User identifier. |
| `lastName` | string | User last name. |
| `securityLevel` | string | User security level. |
| `title` | string | User title. |

## Native endpoint

Through the native 5pm API, this operation is `POST /service/post/users/add` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

