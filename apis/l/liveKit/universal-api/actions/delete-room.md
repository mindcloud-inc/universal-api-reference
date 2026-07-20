# LiveKit: Delete Room

Deletes an existing room from LiveKit.

```
DELETE https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/delete-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/delete-room?connectionId=$CONNECTION_ID&room=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/delete-room?${params}`, {
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
| `room` | string | yes | Name of the room to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LiveKit API returns.

## Native endpoint

Through the native LiveKit API, this operation is `POST /twirp/livekit.RoomService/DeleteRoom` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-room.md) for the provider-specific parameters and requirements.

