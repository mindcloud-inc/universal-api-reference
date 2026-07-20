# LiveKit: Create Room

Creates a new room in LiveKit.

```
POST https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/create-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/create-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/create-room', {
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
| `name` | string | yes | Name of the room to create. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emptyTimeout` | number | no | Seconds to keep the room open if no one joins. |
| `departureTimeout` | number | no | Seconds the room remains open after the last participant leaves. |
| `maxParticipants` | number | no | Maximum participant count; 0 means no limit. |
| `metadata` | string | no | Initial room metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_recording": true,
      "creation_time": "string",
      "creation_time_ms": "string",
      "departure_timeout": 1,
      "empty_timeout": 1,
      "enabled_codecs": [
        {}
      ],
      "max_participants": 1,
      "metadata": "string",
      "name": "Ava Chen",
      "num_participants": 1,
      "num_publishers": 1,
      "sid": "string",
      "version": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_recording` | boolean | Whether recording is active. |
| `creation_time` | string | Room creation timestamp in seconds. |
| `creation_time_ms` | string | Room creation timestamp in milliseconds. |
| `departure_timeout` | number | Seconds before participant departure is finalized. |
| `empty_timeout` | number | Seconds before an empty room is closed. |
| `enabled_codecs` | array<object> | Codecs enabled for the room. |
| `max_participants` | number | Maximum participant count. |
| `metadata` | string | Room metadata string. |
| `name` | string | Room name. |
| `num_participants` | number | Current participant count. |
| `num_publishers` | number | Current publisher count. |
| `sid` | string | LiveKit room SID. |
| `version` | object | Room version metadata. |

## Native endpoint

Through the native LiveKit API, this operation is `POST /twirp/livekit.RoomService/CreateRoom` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-room.md) for the provider-specific parameters and requirements.

