# Liveblocks: Get Room

Retrieves a room from Liveblocks.

```
GET https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-room?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-room?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | string | no | ID of the room. |

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

Through the native Liveblocks API, this operation is `GET /rooms/:roomId` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-room.md) for the provider-specific parameters and requirements.

