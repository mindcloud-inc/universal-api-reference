# Morph: Search Code With WarpGrep

Searches code with Morph WarpGrep.

```
GET https://connect.mindcloud.co/v1/universal/morph/latest/actions/search-code-with-warp-grep
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morph/latest/actions/search-code-with-warp-grep?connectionId=$CONNECTION_ID&messages%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messages[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morph/latest/actions/search-code-with-warp-grep?${params}`, {
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
| `messages[]` | array<object> | yes | WarpGrep conversation containing the system prompt, user search request, and any tool-call turns. |
| `temperature` | number | no | Sampling temperature. Use 0 for deterministic search behavior. Default: `0`. |
| `maxTokens` | number | no | Maximum number of tokens to generate per response. Default: `2048`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Morph API returns.

## Native endpoint

Through the native Morph API, this operation is `POST /chat/completions` (base URL `https://api.morphllm.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-code-with-warp-grep.md) for the provider-specific parameters and requirements.

