# ChatBotKit: Receive AI Response



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/receive-ai-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/receive-ai-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/receive-ai-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | The ID of the conversation to receive a response from |
| `functions[]` | array | no | Functions available during receive |
| `extensions` | object | no | Extensions for the receive request |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
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
| `id` | string |  |
| `text` | string |  |
| `usage.token` | number |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /conversation/{conversationId}/receive` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/receive-ai-response.md) for the provider-specific parameters and requirements.

