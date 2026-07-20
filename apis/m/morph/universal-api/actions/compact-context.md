# Morph: Compact Context

Compacts context with Morph.

```
GET https://connect.mindcloud.co/v1/universal/morph/latest/actions/compact-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morph/latest/actions/compact-context?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morph/latest/actions/compact-context?${params}`, {
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
| `input` | string | yes | Text or code context to compact. |
| `query` | string | no | Optional focus query that tells Morph what context to preserve. |
| `compressionRatio` | number | no | Fraction of the original input to keep, where lower values compress more aggressively. Default: `0.5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Morph API returns.

## Native endpoint

Through the native Morph API, this operation is `POST /compact` (base URL `https://api.morphllm.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compact-context.md) for the provider-specific parameters and requirements.

