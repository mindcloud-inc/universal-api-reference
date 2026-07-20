# ChatBotKit: Complete Conversation Interaction



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/complete-conversation-interaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/complete-conversation-interaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/complete-conversation-interaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[]` | array | yes | Messages to complete |
| `attachments[]` | array | no | Attachments for the completion request |
| `contactId` | object | no | Contact payload for the completion request |
| `functions[]` | array | no | Functions available during completion |
| `extensions` | object | no | Extensions for the completion request |
| `limits` | object | no | Execution limits for the completion request |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": {
        "reason": "string"
      },
      "text": "string",
      "usage": {
        "token": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end.reason` | string |  |
| `text` | string |  |
| `usage.token` | number |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /conversation/complete` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-conversation-interaction.md) for the provider-specific parameters and requirements.

