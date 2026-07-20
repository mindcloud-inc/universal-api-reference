# Element: Leave Room

Leaves a room in Element for the current user.

```
PUT https://connect.mindcloud.co/v1/universal/element/latest/actions/leave-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/element/latest/actions/leave-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/element/latest/actions/leave-room', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | string | yes | Room ID to leave. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Element API returns.

## Native endpoint

Through the native Element API, this operation is `POST /_matrix/client/v3/rooms/:roomId/leave` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/leave-room.md) for the provider-specific parameters and requirements.

