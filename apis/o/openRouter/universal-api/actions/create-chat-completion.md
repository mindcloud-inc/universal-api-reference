# OpenRouter: Create Chat Completion

Creates a chat completion in OpenRouter.

```
POST https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRouter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/create-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "messages[]": [
    {}
  ],
  "messages[].content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/create-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "messages[]": [{}],
    "messages[].content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | OpenRouter model identifier, for example openai/gpt-5.2. |
| `messages[]` | array<object> | yes | Conversation messages sent to the chat completion endpoint. |
| `messages[].content` | string | yes | Text content for the message. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `temperature` | number | no | Sampling temperature. |
| `maxTokens` | number | no | Maximum number of completion tokens. |
| `stream` | boolean | no | Whether to stream incremental tokens. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OpenRouter API returns.

## Native endpoint

Through the native OpenRouter API, this operation is `POST /chat/completions` (base URL `https://openrouter.ai/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

