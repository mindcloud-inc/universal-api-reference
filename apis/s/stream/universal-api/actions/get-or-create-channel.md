# Stream: Get Or Create Channel

Finds a channel in Stream, or creates it if needed.

```
POST https://connect.mindcloud.co/v1/universal/stream/latest/actions/get-or-create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stream/latest/actions/get-or-create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stream/latest/actions/get-or-create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Channel type. |
| `id` | string | yes | Channel ID. |
| `data` | object | no | Channel creation/update payload. |
| `state` | boolean | no | Whether to return channel state. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {},
      "duration": "string",
      "members": [
        {}
      ],
      "messages": [
        {}
      ],
      "pinnedMessages": [
        {}
      ],
      "read": [
        {}
      ],
      "threads": [
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
| `channel` | object |  |
| `duration` | string |  |
| `members` | array<object> |  |
| `messages` | array<object> |  |
| `pinnedMessages` | array<object> |  |
| `read` | array<object> |  |
| `threads` | array<object> |  |

## Native endpoint

Through the native Stream API, this operation is `POST /channels/:type/:id/query` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-or-create-channel.md) for the provider-specific parameters and requirements.

