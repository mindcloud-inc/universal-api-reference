# Liveblocks: Subscribe To Thread

Updates a Liveblocks thread subscription by subscribing a user.

```
PUT https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/subscribe-to-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/subscribe-to-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/subscribe-to-thread', {
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
      "createdAt": "string",
      "kind": "string",
      "subjectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `kind` | string |  |
| `subjectId` | string |  |

## Native endpoint

Through the native Liveblocks API, this operation is `POST /rooms/:roomId/threads/:threadId/subscribe` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-thread.md) for the provider-specific parameters and requirements.

