# Zoho Cliq: Retrieve Chat Message

Retrieves a chat message from Zoho Cliq by ID.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-chat-message?connectionId=$CONNECTION_ID&chatId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-chat-message?${params}`, {
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
| `chatId` | string | yes | The ID of the chat containing the message. |
| `messageId` | string | yes | The ID of the message to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "id": "string",
      "is_pinned": true,
      "is_read": true,
      "revision": 1,
      "sender": {},
      "time": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object | The message content payload. |
| `id` | string | The message identifier. |
| `is_pinned` | boolean | Whether the message is pinned. |
| `is_read` | boolean | Whether the message has been read. |
| `revision` | number | The message revision. |
| `sender` | object | The sender details. |
| `time` | number | The message time in milliseconds. |
| `type` | string | The message type. |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /chats/:chatId/messages/:messageId` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-chat-message.md) for the provider-specific parameters and requirements.

