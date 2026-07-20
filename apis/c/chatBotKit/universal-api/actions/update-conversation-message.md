# ChatBotKit: Update Conversation Message



```
PUT https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/update-conversation-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/update-conversation-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/update-conversation-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | The ID of the conversation |
| `messageId` | string | yes | The ID of the message to update |
| `name` | string | no | Name of the message |
| `description` | string | no | Description of the message |
| `meta` | object | no | Metadata for the message |
| `type` | list | no | Type of the message One of: `activity`, `backstory`, `bot`, `context`, `instruction`, `reasoning`, `user`. |
| `text` | string | no | Text of the message |
| `entities[]` | array | no | Entities attached to the message |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /conversation/{conversationId}/message/{messageId}/update` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-message.md) for the provider-specific parameters and requirements.

