# Usedesk: Send Chat Message

Sends a chat message in Usedesk.

```
POST https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/send-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/send-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": 1,
  "userId": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/send-chat-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": 1,
    "userId": 1,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | number | yes | Chat ID. |
| `userId` | number | yes | Agent ID on whose behalf the message will be sent. |
| `text` | string | yes | Message text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /chat/sendMessage` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-chat-message.md) for the provider-specific parameters and requirements.

