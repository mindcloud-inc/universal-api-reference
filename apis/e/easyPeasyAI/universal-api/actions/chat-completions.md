# Easy-Peasy.AI: Chat Completions

Creates a chat completion in Easy-Peasy.AI.

```
POST https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/chat-completions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy-Peasy.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/chat-completions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/chat-completions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[]` | array<object> | yes | The chat message array in OpenAI-compatible format with role and content per item. |
| `model` | string | no | Optional chat model override such as gpt-4.1-mini. |
| `stream` | boolean | no | Enable streaming server-sent events. |
| `temperature` | number | no | Optional sampling temperature from 0 to 2. |
| `maxTokens` | number | no | Optional maximum number of tokens to generate. |
| `topP` | number | no | Optional nucleus sampling parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy-Peasy.AI API returns.

## Native endpoint

Through the native Easy-Peasy.AI API, this operation is `POST /api/chat/completions` (base URL `https://easy-peasy.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chat-completions.md) for the provider-specific parameters and requirements.

