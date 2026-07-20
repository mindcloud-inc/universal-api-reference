# Chatling: List Conversations

Retrieves conversations from Chatling.

```
GET https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-conversations?connectionId=$CONNECTION_ID&chatbotId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-conversations?${params}`, {
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
| `sort` | string | no | The sort order for the conversations list. Default: `date_desc`. |

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

Through the native Chatling API, this operation is `GET /chatbots/:chatbotId/conversations` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

