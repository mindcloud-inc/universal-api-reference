# Chatling: Update Chatbot Settings

Updates chatbot settings in Chatling.

```
PUT https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-chatbot-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-chatbot-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-chatbot-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatbotId` | string | yes | The chatbot ID. |
| `name` | string | no | The chatbot name. Example: `Codex Stage 3 Test Chatbot 2026-03-20 15:25`. |
| `visibility` | string | no | The visibility of the chatbot. Example: `public`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "version": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `version` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Chatling API, this operation is `PATCH /chatbots/:chatbotId` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chatbot-settings.md) for the provider-specific parameters and requirements.

