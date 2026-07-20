# ProxyAPI: Custom-Tool Chat Completion

Creates a custom-tool chat completion in ProxyAPI.

```
POST https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/custom-tool-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxyAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/custom-tool-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "gpt-5-nano",
  "messages[0].content": "Use the shell_command tool to produce a command that prints hello."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/custom-tool-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "gpt-5-nano",
    "messages[0].content": "Use the shell_command tool to produce a command that prints hello."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Model id that supports custom-tool chat completions when the account has sufficient balance. Default: `gpt-5-nano`. Example: `gpt-5-nano`. |
| `messages[0].content` | string | yes | Prompt that should trigger the custom tool call. Default: `Use the shell_command tool to produce a command that prints hello.`. Example: `Use the shell_command tool to produce a command that prints hello.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProxyAPI API returns.

## Native endpoint

Through the native ProxyAPI API, this operation is `POST /chat/completions` (base URL `https://openai.api.proxyapi.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/custom-tool-chat-completion.md) for the provider-specific parameters and requirements.

