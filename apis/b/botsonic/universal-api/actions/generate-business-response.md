# Botsonic: Generate Business Response

Generates a business chatbot response in Botsonic.

```
POST https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/generate-business-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/generate-business-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputText": "How do I reset my password?",
  "chatId": "customer-chat-123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/generate-business-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputText": "How do I reset my password?",
    "chatId": "customer-chat-123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputText` | string | yes | User question for the bot. Example: `How do I reset my password?`. |
| `chatId` | string | yes | Chat identifier for the conversation. Example: `customer-chat-123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stream` | boolean | no | Set true to stream data; false for standard retrieval. |
| `source` | string | no | Optional sources for the bot to reference. |
| `starterQuestionId` | string | no | Starter question identifier. |
| `isBusinessApiRequest` | boolean | no | Whether this is a business API request. |
| `isIntegrationRequest` | boolean | no | Whether this is an integration request. |
| `integrationUserIdentifier` | string | no | Integration user unique identifier. |
| `userUniqueIdentifier` | string | no | Additional user identifier stored with the inbox conversation. |
| `chatHistory[]` | array<object> | no | Previous chat history for reference. |
| `chatUserId` | string | no | Chat user identifier linked with existing user data. |
| `extraMetadata` | object | no | Additional metadata for the chat. |
| `fullHistory` | boolean | no | Return the full chat history when true. |
| `messageId` | string | no | Message identifier used to resolve handoff. |
| `timeout` | number | no | Maximum seconds to keep the connection open while generating a response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "chat_ended": true,
      "chat_history": [
        {}
      ],
      "end_chat_feedback": "string",
      "follow_up_questions": [
        "string"
      ],
      "generated_images": [
        "string"
      ],
      "human_handoff_status": true,
      "message_id": "string",
      "sources": [
        {}
      ],
      "user_options": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | Generated answer text. |
| `chat_ended` | boolean | Whether the chat has ended. |
| `chat_history` | array<object> | Full chat history returned by Botsonic. |
| `end_chat_feedback` | string | End chat feedback text. |
| `follow_up_questions` | array<string> | Suggested follow-up questions. |
| `generated_images` | array<string> | Generated image URLs or identifiers. |
| `human_handoff_status` | boolean | Whether human handoff is active. |
| `message_id` | string | Generated response message identifier. |
| `sources` | array<object> | Sources used by the answer. |
| `user_options` | array<string> | User options returned by Botsonic. |

## Native endpoint

Through the native Botsonic API, this operation is `POST /v1/business/botsonic` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-business-response.md) for the provider-specific parameters and requirements.

