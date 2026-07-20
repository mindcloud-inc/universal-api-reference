# ProxyAPI: Stream Chat Completion

Streams a chat completion from ProxyAPI.

```
POST https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/stream-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxyAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/stream-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "openrouter/openrouter/free",
  "messages[0].content": "Reply with only the word hello."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/stream-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "openrouter/openrouter/free",
    "messages[0].content": "Reply with only the word hello."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | OpenAI-compatible model id to run through ProxyAPI. Default: `openrouter/openrouter/free`. Example: `openrouter/openrouter/free`. |
| `messages[0].content` | string | yes | Prompt text for the streamed chat completion. Example: `Reply with only the word hello.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Raw server-sent events payload returned by the streaming chat completion request. |

## Native endpoint

Through the native ProxyAPI API, this operation is `POST /chat/completions` (base URL `https://openai.api.proxyapi.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-chat-completion.md) for the provider-specific parameters and requirements.

