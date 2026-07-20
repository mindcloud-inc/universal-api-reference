# Chatling: Retrieve Conversation

Retrieves a conversation from Chatling.

```
GET https://connect.mindcloud.co/v1/universal/chatling/latest/actions/retrieve-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/retrieve-conversation?connectionId=$CONNECTION_ID&chatbotId=string&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotId": "string",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatling/latest/actions/retrieve-conversation?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": 1,
      "contactId": "string",
      "conversationType": "string",
      "createdAt": "string",
      "id": "string",
      "important": 1,
      "messages": [
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
| `archived` | number | Whether the conversation is archived. |
| `contactId` | string | The contact associated with the conversation. |
| `conversationType` | string | The type of the conversation. |
| `createdAt` | string | The date and time when the conversation was created. |
| `id` | string | The unique identifier of the conversation. |
| `important` | number | Whether the conversation is marked as important. |
| `messages` | array<object> | The messages included in the conversation response. |

## Native endpoint

Through the native Chatling API, this operation is `GET /chatbots/:chatbotId/conversations/:conversationId` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-conversation.md) for the provider-specific parameters and requirements.

