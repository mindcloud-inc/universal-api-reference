# Hex: Create Collection



```
POST https://connect.mindcloud.co/v1/universal/hex/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hex/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hex/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |
| `name` | string | yes |  |
| `sharing.groups[].access` | string<string> | no |  |
| `sharing.groups[].id` | string<string> | no |  |
| `sharing.users[].access` | string<string> | no |  |
| `sharing.users[].id` | string<string> | no |  |
| `sharing.workspace.members` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator": {
        "email": "ava@example.com",
        "id": "string"
      },
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "sharing": {
        "groups": [
          {}
        ],
        "users": [
          {}
        ],
        "workspace": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator.email` | string |  |
| `creator.id` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `sharing.groups` | array<object> |  |
| `sharing.users` | array<object> |  |
| `sharing.workspace` | object |  |

## Native endpoint

Through the native Hex API, this operation is `POST /collections` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

