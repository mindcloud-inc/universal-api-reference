# Zoom Team Chat: Send Chat Message



```
POST https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/send-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/send-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "me",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/send-chat-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "me",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The unique identifier of the user. Default: `me`. |
| `message` | string | yes | The message content. |
| `toContact` | string | no | The contact email address for a 1:1 message. |
| `toChannel` | string | no | The channel ID for a channel message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_time": "string",
      "id": "string",
      "message": "string",
      "sender": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_time` | string |  |
| `id` | string |  |
| `message` | string |  |
| `sender` | object |  |

## Native endpoint

Through the native Zoom Team Chat API, this operation is `POST /chat/users/:userId/messages` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-chat-message.md) for the provider-specific parameters and requirements.

