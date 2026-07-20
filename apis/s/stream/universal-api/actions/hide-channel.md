# Stream: Hide Channel

Hides a channel in Stream.

```
PUT https://connect.mindcloud.co/v1/universal/stream/latest/actions/hide-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stream/latest/actions/hide-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "id": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stream/latest/actions/hide-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "id": "string",
    "userId": "string"
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
| `clearHistory` | boolean | no | Whether to clear message history when hiding the channel. |
| `userId` | string | yes | User ID performing the hide operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | string |  |

## Native endpoint

Through the native Stream API, this operation is `POST /channels/:type/:id/hide` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/hide-channel.md) for the provider-specific parameters and requirements.

