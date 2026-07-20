# Innform: Invite User

Invites a new user to Innform.

```
POST https://connect.mindcloud.co/v1/universal/innform/latest/actions/invite-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/innform/latest/actions/invite-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/innform/latest/actions/invite-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address for the invited user. |
| `groups[]` | array<string> | no | Optional list of group names. Accepts multiple values as an array. |
| `mobile` | string | no | Optional mobile number. |
| `name` | string | yes | Full name for the invited user. |
| `property` | string | no | Property name to assign to the user. |
| `role` | string | no | Role value: admin or student. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "groups": [
        {}
      ],
      "id": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "property": {},
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `property` | object |  |
| `role` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Innform API, this operation is `POST /users` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-user.md) for the provider-specific parameters and requirements.

