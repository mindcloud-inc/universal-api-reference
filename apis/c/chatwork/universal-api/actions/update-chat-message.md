# Chatwork: Update Chat Message



```
PUT https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "12345",
  "messageId": "101",
  "body": "Hello Chatwork!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "12345",
    "messageId": "101",
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
| `messageId` | string | yes | Message ID Example: `101`. |
| `body` | string | yes | Updated message body Example: `Hello Chatwork!`. |

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

Through the native Chatwork API, this operation is `PUT /rooms/:room_id/messages/:message_id` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat-message.md) for the provider-specific parameters and requirements.

