# ProxyAPI: Parallel Tool-Calling Chat

Creates a parallel tool-calling chat in ProxyAPI.

```
POST https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/parallel-tool-calling-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxyAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/parallel-tool-calling-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "openrouter/openrouter/free",
  "messages[0].content": "Call both tools. Use get_weather for Sao Paulo and get_time for America/Sao_Paulo."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/parallel-tool-calling-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "openrouter/openrouter/free",
    "messages[0].content": "Call both tools. Use get_weather for Sao Paulo and get_time for America/Sao_Paulo."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Model id to run through ProxyAPI. Default: `openrouter/openrouter/free`. Example: `openrouter/openrouter/free`. |
| `messages[0].content` | string | yes | Prompt that should trigger multiple tool calls. Default: `Call both tools. Use get_weather for Sao Paulo and get_time for America/Sao_Paulo.`. Example: `Call both tools. Use get_weather for Sao Paulo and get_time for America/Sao_Paulo.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {}
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "provider": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> |  |
| `created` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `provider` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native ProxyAPI API, this operation is `POST /chat/completions` (base URL `https://openai.api.proxyapi.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parallel-tool-calling-chat.md) for the provider-specific parameters and requirements.

