# Helpjuice: Create User

Creates a new user in Helpjuice.

```
POST https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user.email": "ava@example.com",
  "user.role_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user.email": "ava@example.com",
    "user.role_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user.email` | string | yes | The Helpjuice user email. |
| `user.first_name` | string | no | The Helpjuice user first name. |
| `user.last_name` | string | no | The Helpjuice user last name. |
| `user.role_id` | string | yes | The Helpjuice role id for the user. Observed valid values include viewer and admin. |
| `user` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user` | object |  |

## Native endpoint

Through the native Helpjuice API, this operation is `POST /users` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

