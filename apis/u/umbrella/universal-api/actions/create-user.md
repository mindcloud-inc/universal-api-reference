# Umbrella: Create User

Creates a new user in Umbrella.

```
POST https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-user', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | The user's email address. |
| `firstname` | string | no | The user's first name. |
| `lastname` | string | no | The user's last name. |
| `password` | string | no | The user's password. |
| `roleId` | string | no | The Umbrella role ID. |
| `timezone` | string | no | A valid IANA timezone like America/New_York. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "lastname": "Chen",
      "role": "string",
      "roleId": 1,
      "status": "string",
      "timezone": "string",
      "twoFactorEnable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `lastname` | string |  |
| `role` | string |  |
| `roleId` | number |  |
| `status` | string |  |
| `timezone` | string |  |
| `twoFactorEnable` | boolean |  |

## Native endpoint

Through the native Umbrella API, this operation is `POST https://api.umbrella.com/admin/v2/users` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

