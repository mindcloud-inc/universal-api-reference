# Tinq.ai: Search Workspace



```
GET https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/search-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/search-workspace?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/search-workspace?${params}`, {
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
| `query` | string | yes | Search query text. |
| `topK` | number | no | Maximum number of results to return. Default: `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tinq.ai API returns.

## Native endpoint

Through the native Tinq.ai API, this operation is `POST /api/v2/search` (base URL `https://tinq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-workspace.md) for the provider-specific parameters and requirements.

