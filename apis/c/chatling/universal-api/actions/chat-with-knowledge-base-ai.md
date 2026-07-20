# Chatling: Chat With Knowledge Base AI

Chats with Chatling's knowledge base AI.

```
GET https://connect.mindcloud.co/v1/universal/chatling/latest/actions/chat-with-knowledge-base-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/chat-with-knowledge-base-ai?connectionId=$CONNECTION_ID&chatbotId=string&message=string&aiModelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotId": "string",
  "message": "string",
  "aiModelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatling/latest/actions/chat-with-knowledge-base-ai?${params}`, {
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
| `message` | string | yes | The message to send to the AI. |
| `aiModelId` | number | yes | The ID of the AI model to use for the response. |
| `conversationId` | string | no | The conversation ID to continue. Leave blank to create a new conversation. |
| `contactId` | string | no | The contact ID to associate with the conversation. |
| `languageId` | number | no | The ID of the language to use for the AI response. Default: `1`. |
| `temperature` | number | no | The temperature to use for the AI response. Default: `0`. |
| `instructions[]` | array<string> | no | Optional instruction strings to tailor the AI response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": "string",
      "messageId": "string",
      "response": "string",
      "sources": [
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
| `conversationId` | string | The unique identifier of the conversation. |
| `messageId` | string | The unique identifier of the AI response message. |
| `response` | string | The response from the AI. |
| `sources` | array<object> | The sources used by the AI to generate the response. |

## Native endpoint

Through the native Chatling API, this operation is `POST /chatbots/:chatbotId/ai/kb/chat` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chat-with-knowledge-base-ai.md) for the provider-specific parameters and requirements.

