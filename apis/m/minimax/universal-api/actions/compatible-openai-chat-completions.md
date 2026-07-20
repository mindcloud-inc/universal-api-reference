# Minimax: Compatible OpenAI Chat Completions



```
POST https://connect.mindcloud.co/v1/universal/minimax/latest/actions/compatible-openai-chat-completions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minimax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/compatible-openai-chat-completions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ],
  "model": "MiniMax-M2.7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minimax/latest/actions/compatible-openai-chat-completions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}],
    "model": "MiniMax-M2.7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[]` | array<object> | yes | Conversation messages array sent to MiniMax. |
| `model` | string | yes | MiniMax model ID to use for the request. Example: `MiniMax-M2.7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_resp": {
        "status_code": 1,
        "status_msg": "string"
      },
      "choices": {},
      "created": 1,
      "id": "string",
      "input_sensitive": true,
      "input_sensitive_type": 1,
      "model": "string",
      "object": "string",
      "output_sensitive": true,
      "output_sensitive_int": 1,
      "output_sensitive_type": 1,
      "usage": {
        "total_characters": 1,
        "total_tokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_resp.status_code` | number |  |
| `base_resp.status_msg` | string |  |
| `choices` | object |  |
| `created` | number |  |
| `id` | string |  |
| `input_sensitive` | boolean |  |
| `input_sensitive_type` | number |  |
| `model` | string |  |
| `object` | string |  |
| `output_sensitive` | boolean |  |
| `output_sensitive_int` | number |  |
| `output_sensitive_type` | number |  |
| `usage.total_characters` | number |  |
| `usage.total_tokens` | number |  |

## Native endpoint

Through the native Minimax API, this operation is `POST /v1/text/chatcompletion_v2` (base URL `https://api.minimax.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compatible-openai-chat-completions.md) for the provider-specific parameters and requirements.

