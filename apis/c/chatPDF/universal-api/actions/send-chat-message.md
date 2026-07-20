# ChatPDF: Send Chat Message



```
GET https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/send-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/send-chat-message?connectionId=$CONNECTION_ID&sourceId=src_xxxxxx&messages%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "src_xxxxxx",
  "messages[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/send-chat-message?${params}`, {
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
| `sourceId` | string | yes | ChatPDF source ID to query. Example: `src_xxxxxx`. |
| `messages[]` | array<object> | yes | Conversation history array of { role, content } objects. Include all relevant prior messages for follow-up questions. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | ChatPDF answer text. |

## Native endpoint

Through the native ChatPDF API, this operation is `POST /chats/message` (base URL `https://api.chatpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-chat-message.md) for the provider-specific parameters and requirements.

