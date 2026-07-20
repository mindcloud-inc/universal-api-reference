# Langbase: Retrieve Memory Chunks



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/retrieve-memory-chunks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/retrieve-memory-chunks?connectionId=$CONNECTION_ID&memory%5B%5D=%5Bobject%20Object%5D&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memory[]": "[object Object]",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/retrieve-memory-chunks?${params}`, {
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
| `memory[]` | array<object> | yes | Array of memory selectors to search. |
| `query` | string | yes | Question or text to retrieve against the selected memories. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Langbase API returns.

## Native endpoint

Through the native Langbase API, this operation is `POST v1/memory/retrieve` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-memory-chunks.md) for the provider-specific parameters and requirements.

