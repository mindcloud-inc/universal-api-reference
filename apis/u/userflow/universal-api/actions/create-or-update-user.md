# Userflow: Create Or Update User

Creates or updates a user in Userflow.

```
POST https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-or-update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-or-update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-or-update-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier for the user. |
| `attributes` | object | no | User attributes to merge into the Userflow user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "groups": {},
      "id": "string",
      "memberships": {},
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | User attributes. |
| `attributes.email` | string | User email. |
| `attributes.name` | string | User name. |
| `created_at` | date | User creation timestamp. |
| `groups` | object | User groups. |
| `id` | string | User ID. |
| `memberships` | object | User memberships. |
| `object` | string | Returned object type. |

## Native endpoint

Through the native Userflow API, this operation is `POST /users` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-user.md) for the provider-specific parameters and requirements.

