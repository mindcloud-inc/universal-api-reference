# ChatBotKit: Send Conversation Message



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/send-conversation-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/send-conversation-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/send-conversation-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | The ID of the conversation to send the message to |
| `text` | string | yes | Text of the message to send |
| `entities[]` | array | no | Entities attached to the message |
| `functions[]` | array | no | Functions available during send |
| `extensions` | object | no | Extensions for the send request |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {
          "begin": 1,
          "end": 1,
          "replacement": {
            "begin": 1,
            "end": 1,
            "text": "string"
          },
          "text": "string",
          "type": "string"
        }
      ],
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities[].begin` | number |  |
| `entities[].end` | number |  |
| `entities[].replacement.begin` | number |  |
| `entities[].replacement.end` | number |  |
| `entities[].replacement.text` | string |  |
| `entities[].text` | string |  |
| `entities[].type` | string |  |
| `id` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /conversation/{conversationId}/send` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-conversation-message.md) for the provider-specific parameters and requirements.

