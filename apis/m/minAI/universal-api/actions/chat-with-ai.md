# 1minAI: Chat with AI

Creates an AI chat response in 1minAI.

```
POST https://connect.mindcloud.co/v1/universal/minAI/latest/actions/chat-with-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1minAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minAI/latest/actions/chat-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "Explain quantum computing in simple terms"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minAI/latest/actions/chat-with-ai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "Explain quantum computing in simple terms"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Example: `Explain quantum computing in simple terms`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | no |  |
| `webSearch` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiRecord": {},
      "temporaryUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiRecord` | object | Chat execution record. |
| `temporaryUrl` | string | Temporary asset URL when available. |

## Native endpoint

Through the native 1minAI API, this operation is `POST /api/chat-with-ai` (base URL `https://api.1min.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chat-with-ai.md) for the provider-specific parameters and requirements.

