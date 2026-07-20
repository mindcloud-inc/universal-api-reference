# LiveKit: Update Room Metadata

Updates metadata for an existing LiveKit room.

```
PUT https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/update-room-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/update-room-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room": "string",
  "metadata": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/update-room-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room": "string",
    "metadata": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room` | string | yes |  |
| `metadata` | string | yes |  |

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
| `metadata` | string | Updated room metadata string. |
| `name` | string | Room name. |
| `num_participants` | number | Current participant count. |
| `num_publishers` | number | Current publisher count. |
| `sid` | string | LiveKit room SID. |
| `version` | object | Room version metadata. |

## Native endpoint

Through the native LiveKit API, this operation is `POST /twirp/livekit.RoomService/UpdateRoomMetadata` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-room-metadata.md) for the provider-specific parameters and requirements.

