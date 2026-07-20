# Element: Get Room State

Retrieves a room's state from Element.

```
GET https://connect.mindcloud.co/v1/universal/element/latest/actions/get-room-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/element/latest/actions/get-room-state?connectionId=$CONNECTION_ID&roomId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/element/latest/actions/get-room-state?${params}`, {
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
| `roomId` | string | yes | Room ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "content": {},
      "event_id": "string",
      "origin_server_ts": 1,
      "room_id": "string",
      "sender": "string",
      "state_key": "string",
      "type": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number |  |
| `content` | object |  |
| `event_id` | string |  |
| `origin_server_ts` | number |  |
| `room_id` | string |  |
| `sender` | string |  |
| `state_key` | string |  |
| `type` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Element API, this operation is `GET /_matrix/client/v3/rooms/:roomId/state` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-room-state.md) for the provider-specific parameters and requirements.

