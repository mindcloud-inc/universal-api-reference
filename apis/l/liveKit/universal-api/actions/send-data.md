# LiveKit: Send Data

Sends data to participants in a LiveKit room.

```
POST https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/send-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/send-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room": "string",
  "data": "string",
  "kind": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/send-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room": "string",
    "data": "string",
    "kind": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room` | string | yes |  |
| `data` | string | yes | Raw data payload to send. Provide the payload expected by your LiveKit client data handler. |
| `kind` | string | yes | Delivery mode, usually reliable or lossy. |
| `destinationIdentities[]` | array<string> | no |  |
| `topic` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LiveKit API returns.

## Native endpoint

Through the native LiveKit API, this operation is `POST /twirp/livekit.RoomService/SendData` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-data.md) for the provider-specific parameters and requirements.

