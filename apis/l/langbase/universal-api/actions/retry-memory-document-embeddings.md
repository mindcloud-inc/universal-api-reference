# Langbase: Retry Memory Document Embeddings



```
PUT https://connect.mindcloud.co/v1/universal/langbase/latest/actions/retry-memory-document-embeddings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/retry-memory-document-embeddings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memoryName": "Ava Chen",
  "documentName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langbase/latest/actions/retry-memory-document-embeddings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memoryName": "Ava Chen",
    "documentName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memoryName` | string | yes | Memory name that owns the document. |
| `documentName` | string | yes | Document name to retry embeddings for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Langbase API returns.

## Native endpoint

Through the native Langbase API, this operation is `GET v1/memory/:memoryName/documents/:documentName/embeddings/retry` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retry-memory-document-embeddings.md) for the provider-specific parameters and requirements.

