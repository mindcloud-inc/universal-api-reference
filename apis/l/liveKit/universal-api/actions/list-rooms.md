# LiveKit: List Rooms

Retrieves rooms from LiveKit.

```
GET https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-rooms?${params}`, {
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
| `names[]` | array<string> | no | Optional list of room names to return. Default: `[]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rooms": [
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
| `rooms` | array<object> | Active LiveKit rooms returned by ListRooms. |

## Native endpoint

Through the native LiveKit API, this operation is `POST /twirp/livekit.RoomService/ListRooms` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rooms.md) for the provider-specific parameters and requirements.

