# LiveKit: List Participants

Retrieves participants in a LiveKit room.

```
GET https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-participants?connectionId=$CONNECTION_ID&room=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-participants?${params}`, {
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
| `room` | string | yes | Name of the room whose participants should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "participants": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `participants` | array<object> | Participants currently in the room. |

## Native endpoint

Through the native LiveKit API, this operation is `POST /twirp/livekit.RoomService/ListParticipants` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-participants.md) for the provider-specific parameters and requirements.

