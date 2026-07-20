# Anthropic: Count Message Tokens

Counts tokens in an Anthropic message request.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/count-message-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/count-message-tokens?connectionId=$CONNECTION_ID&model=claude-sonnet-4-5-20250929&messages%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "model": "claude-sonnet-4-5-20250929",
  "messages[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/count-message-tokens?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | The model that would complete your prompt. Example: `claude-sonnet-4-5-20250929`. |
| `messages[]` | array<object> | yes | Input conversation messages. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `system` | string | no | System prompt content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inputTokens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inputTokens` | number |  |

## Native endpoint

Through the native Anthropic API, this operation is `POST /v1/messages/count_tokens` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-message-tokens.md) for the provider-specific parameters and requirements.

