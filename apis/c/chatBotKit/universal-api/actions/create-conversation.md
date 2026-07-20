# ChatBotKit: Create Conversation



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name of the conversation |
| `description` | string | no | Description of the conversation |
| `meta` | object | no | Metadata for the conversation |
| `contactId` | string | no | Contact ID for the conversation |
| `taskId` | string | no | Task ID for the conversation |
| `spaceId` | string | no | Space ID for the conversation |
| `messages[]` | array | no | Messages used to create the conversation |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "messages": [
        {
          "text": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `messages[].text` | string |  |
| `messages[].type` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /conversation/create` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

