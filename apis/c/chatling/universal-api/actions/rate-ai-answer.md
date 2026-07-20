# Chatling: Rate AI Answer

Rates an AI answer in Chatling.

```
PUT https://connect.mindcloud.co/v1/universal/chatling/latest/actions/rate-ai-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/rate-ai-answer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotId": "string",
  "conversationId": "string",
  "messageId": "string",
  "rating": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatling/latest/actions/rate-ai-answer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotId": "string",
    "conversationId": "string",
    "messageId": "string",
    "rating": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatbotId` | string | yes | The chatbot ID. |
| `conversationId` | string | yes | The conversation ID. |
| `messageId` | string | yes | The message ID. |
| `rating` | string | yes | The rating to apply: 0 remove, 1 helpful, -1 not helpful. Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatling API returns.

## Native endpoint

Through the native Chatling API, this operation is `PATCH /chatbots/:chatbotId/conversations/:conversationId/messages/:messageId/rate-ai-answer` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rate-ai-answer.md) for the provider-specific parameters and requirements.

