# Swit: Create User

Creates a new user in Swit.

```
POST https://connect.mindcloud.co/v1/universal/swit/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swit/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userName": "Ava Chen",
  "userEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swit/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userName": "Ava Chen",
    "userEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | Language for the new user. |
| `timezone` | string | no | Timezone for the new user. |
| `userName` | string | yes | Display name for the user. |
| `userEmail` | string | yes | Email address for the user. |
| `tel` | string | no | Telephone number for the user. |
| `msg` | string | no | Optional profile message for the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user_id` | string |  |

## Native endpoint

Through the native Swit API, this operation is `POST organization.user.create` (base URL `https://openapi.swit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

