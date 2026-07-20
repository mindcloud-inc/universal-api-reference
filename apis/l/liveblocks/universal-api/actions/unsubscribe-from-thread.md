# Liveblocks: Unsubscribe From Thread

Updates a Liveblocks thread subscription by unsubscribing a user.

```
PUT https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/unsubscribe-from-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/unsubscribe-from-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/unsubscribe-from-thread', {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the thread unsubscribe request succeeded. |

## Native endpoint

Through the native Liveblocks API, this operation is `POST /rooms/:roomId/threads/:threadId/unsubscribe` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-from-thread.md) for the provider-specific parameters and requirements.

