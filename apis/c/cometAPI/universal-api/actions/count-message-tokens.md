# CometAPI: Count Message Tokens



```
GET https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/count-message-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/count-message-tokens?connectionId=$CONNECTION_ID&messages%5B%5D=%5Bobject%20Object%5D&model=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messages[]": "[object Object]",
  "model": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/count-message-tokens?${params}`, {
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
| `messages[]` | array<object> | yes | Anthropic message turns to count. |
| `model` | string | yes | Anthropic-compatible model ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input_tokens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input_tokens` | number |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /v1/messages/count_tokens` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-message-tokens.md) for the provider-specific parameters and requirements.

