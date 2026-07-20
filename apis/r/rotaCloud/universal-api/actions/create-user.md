# RotaCloud: Create User

Creates a user in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "first_name": "Ava",
  "last_name": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "first_name": "Ava",
    "last_name": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `first_name` | string | yes | User first name. |
| `last_name` | string | yes | User last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "default_role": 1,
      "deleted": true,
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "level": "string",
      "locations": [
        1
      ],
      "roles": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `default_role` | number |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `level` | string |  |
| `locations` | array<number> |  |
| `roles` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/users` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

