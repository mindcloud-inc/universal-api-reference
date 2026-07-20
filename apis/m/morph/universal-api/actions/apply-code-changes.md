# Morph: Apply Code Changes

Applies code changes with Morph.

```
GET https://connect.mindcloud.co/v1/universal/morph/latest/actions/apply-code-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morph/latest/actions/apply-code-changes?connectionId=$CONNECTION_ID&messages%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messages[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morph/latest/actions/apply-code-changes?${params}`, {
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
| `messages[]` | array<object> | yes | Single-message Apply payload using Morph's required structured format. |
| `temperature` | number | no | Sampling temperature. Use 0 for deterministic edits. Default: `0`. |
| `maxTokens` | number | no | Maximum number of tokens to generate. Default: `256`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Morph API returns.

## Native endpoint

Through the native Morph API, this operation is `POST /chat/completions` (base URL `https://api.morphllm.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-code-changes.md) for the provider-specific parameters and requirements.

