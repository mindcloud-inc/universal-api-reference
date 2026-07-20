# ChatBotKit: Create Conversation Message



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-conversation-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-conversation-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "type": "activity",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-conversation-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "type": "activity",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | The ID of the conversation |
| `name` | string | no | Name of the message |
| `description` | string | no | Description of the message |
| `meta` | object | no | Metadata for the message |
| `type` | list | yes | Type of the message One of: `activity`, `backstory`, `bot`, `context`, `instruction`, `reasoning`, `user`. |
| `text` | string | yes | Text of the message |
| `entities[]` | array | no | Entities attached to the message |

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

Through the native ChatBotKit API, this operation is `POST /conversation/{conversationId}/message/create` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation-message.md) for the provider-specific parameters and requirements.

