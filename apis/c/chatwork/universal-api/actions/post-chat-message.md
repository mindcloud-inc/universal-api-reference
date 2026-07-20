# Chatwork: Post Chat Message



```
POST https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/post-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/post-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "12345",
  "body": "Hello Chatwork!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/post-chat-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "12345",
    "body": "Hello Chatwork!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Room ID Example: `12345`. |
| `body` | string | yes | Message body Example: `Hello Chatwork!`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `selfUnread` | list<number> | no | Whether to mark the posted message as unread for yourself One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageId` | string |  |

## Native endpoint

Through the native Chatwork API, this operation is `POST /rooms/:room_id/messages` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-chat-message.md) for the provider-specific parameters and requirements.

