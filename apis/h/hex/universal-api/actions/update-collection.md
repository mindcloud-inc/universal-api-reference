# Hex: Update Collection



```
PUT https://connect.mindcloud.co/v1/universal/hex/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hex/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hex/latest/actions/update-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Unique ID for a collection. |
| `description` | string | no |  |
| `name` | string | no |  |
| `sharing.upsert.groups[].access` | string<string> | no |  |
| `sharing.upsert.groups[].id` | string<string> | no |  |
| `sharing.upsert.users[].access` | string<string> | no |  |
| `sharing.upsert.users[].id` | string<string> | no |  |
| `sharing.upsert.workspace.members` | string | no |  |

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

Through the native Hex API, this operation is `PATCH /collections/{collectionId}` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.

