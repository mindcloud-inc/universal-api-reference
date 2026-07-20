# ChatBotKit: Create Bot Session



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-bot-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-bot-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-bot-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | The ID of the bot to create a session for |
| `durationInSeconds` | number | no | Session duration in seconds |
| `messages[]` | array | no | Messages used to initialize the session |
| `meta` | object | no | Metadata for the session |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": "string",
      "expiresAt": 1,
      "id": "string",
      "messages": [
        {
          "text": "string",
          "type": "string"
        }
      ],
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | string |  |
| `expiresAt` | number |  |
| `id` | string |  |
| `messages[].text` | string |  |
| `messages[].type` | string |  |
| `token` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /bot/{botId}/session/create` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bot-session.md) for the provider-specific parameters and requirements.

