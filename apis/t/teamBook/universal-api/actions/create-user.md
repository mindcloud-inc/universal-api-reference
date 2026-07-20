# TeamBook: Create User

Creates a new user in TeamBook.

```
POST https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com",
  "role": "string",
  "billable": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com",
    "role": "string",
    "billable": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | The user's first name. |
| `lastName` | string | yes | The user's last name. |
| `email` | string | yes | The user's email address. |
| `role` | string | yes | The TeamBook role for the user. |
| `billable` | boolean | yes | Whether the user is billable. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TeamBook API returns.

## Native endpoint

Through the native TeamBook API, this operation is `POST /users` (base URL `https://web.teambookapp.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

