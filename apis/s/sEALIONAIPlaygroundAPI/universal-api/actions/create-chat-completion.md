# SEA-LION AI Playground: Create Chat Completion



```
POST https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEA-LION AI Playground `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/create-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "messages[]": [
    {}
  ],
  "messages[].content": "string",
  "messages[].role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/create-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "messages[]": [{}],
    "messages[].content": "string",
    "messages[].role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes |  |
| `messages[]` | array<object> | yes |  |
| `messages[].content` | string | yes |  |
| `messages[].role` | string | yes |  |
| `temperature` | number | no |  |
| `maxTokens` | number | no |  |
| `stream` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SEA-LION AI Playground API returns.

## Native endpoint

Through the native SEA-LION AI Playground API, this operation is `POST /chat/completions` (base URL `https://api.sea-lion.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

