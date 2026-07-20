# Chatling: List Conversation Messages

Retrieves conversation messages from Chatling.

```
GET https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-conversation-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-conversation-messages?connectionId=$CONNECTION_ID&chatbotId=string&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotId": "string",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-conversation-messages?${params}`, {
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
| `chatbotId` | string | yes | The chatbot ID. |
| `conversationId` | string | yes | The conversation ID. |
| `sort` | string | no | The sort order for the conversation messages list. Default: `date_desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "data": {},
      "id": "string",
      "isAiKbResponse": true,
      "role": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | The date and time when the message was created. |
| `data` | object | Additional data associated with the message. |
| `id` | string | The unique identifier of the message. |
| `isAiKbResponse` | boolean | Whether the message is AI generated and uses the knowledge base. |
| `role` | string | The role of the sender of the message. |
| `text` | string | The text content of the message. |

## Native endpoint

Through the native Chatling API, this operation is `GET /chatbots/:chatbotId/conversations/:conversationId/messages` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-messages.md) for the provider-specific parameters and requirements.

