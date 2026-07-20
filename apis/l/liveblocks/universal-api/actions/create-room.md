# Liveblocks: Create Room

Creates a new room in Liveblocks.

```
POST https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/create-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/create-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/create-room', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "defaultAccesses": [
        "string"
      ],
      "groupsAccesses": {},
      "id": "string",
      "lastConnectionAt": "string",
      "metadata": {},
      "type": "string",
      "usersAccesses": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `defaultAccesses` | array<string> |  |
| `groupsAccesses` | object |  |
| `id` | string |  |
| `lastConnectionAt` | string |  |
| `metadata` | object |  |
| `type` | string |  |
| `usersAccesses` | object |  |

## Native endpoint

Through the native Liveblocks API, this operation is `POST /rooms` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-room.md) for the provider-specific parameters and requirements.

