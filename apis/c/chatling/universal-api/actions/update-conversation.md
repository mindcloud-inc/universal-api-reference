# Chatling: Update Conversation

Updates an existing conversation in Chatling.

```
PUT https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotId": "string",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotId": "string",
    "conversationId": "string"
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
| `archive` | boolean | no | Whether to archive the conversation. |
| `important` | boolean | no | Whether to mark the conversation as important. |
| `contactId` | string | no | The contact ID to associate with the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": 1,
      "contactId": "string",
      "createdAt": "string",
      "id": "string",
      "important": 1
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
| `createdAt` | string | The date and time when the conversation was created. |
| `id` | string | The unique identifier of the conversation. |
| `important` | number | Whether the conversation is marked as important. |

## Native endpoint

Through the native Chatling API, this operation is `PATCH /chatbots/:chatbotId/conversations/:conversationId` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

