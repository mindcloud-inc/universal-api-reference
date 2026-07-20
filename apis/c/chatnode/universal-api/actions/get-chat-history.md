# Chatnode: Get Chat History



```
GET https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/get-chat-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatnode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/get-chat-history?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/get-chat-history?${params}`, {
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
| `botId` | string | yes | The Chatnode agent id associated with the trained agent model. |
| `conversationSessionIds` | string | no | Conversation session ids to include in the raw JSON array request body documented by Chatnode. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": "string",
      "message": {
        "data": {
          "content": "string",
          "type": "string"
        },
        "type": "string"
      },
      "session_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Timestamp when the message was created. |
| `id` | string | Unique identifier for the chat message. |
| `message.data.content` | string | Message content returned by the chatbot. |
| `message.data.type` | string | Nested message data type. |
| `message.type` | string | Top-level message type. |
| `session_id` | string | Chat session identifier. |

## Native endpoint

Through the native Chatnode API, this operation is `POST get-chats/:botId` (base URL `https://api.public.chatnode.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-history.md) for the provider-specific parameters and requirements.

