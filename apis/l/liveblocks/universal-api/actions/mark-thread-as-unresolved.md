# Liveblocks: Mark Thread As Unresolved

Marks a thread as unresolved in Liveblocks.

```
PUT https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/mark-thread-as-unresolved
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/mark-thread-as-unresolved" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/mark-thread-as-unresolved', {
  method: 'PUT',
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
| `roomId` | string | no | ID of the room. |
| `threadId` | string | no | ID of the thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "createdAt": "string",
      "id": "string",
      "metadata": {},
      "resolved": true,
      "roomId": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `createdAt` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `resolved` | boolean |  |
| `roomId` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Liveblocks API, this operation is `POST /rooms/:roomId/threads/:threadId/mark-as-unresolved` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-thread-as-unresolved.md) for the provider-specific parameters and requirements.

