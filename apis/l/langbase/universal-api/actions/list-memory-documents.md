# Langbase: List Memory Documents



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-memory-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-memory-documents?connectionId=$CONNECTION_ID&memoryName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memoryName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-memory-documents?${params}`, {
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
| `memoryName` | string | yes | Memory name to list documents for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Langbase API returns.

## Native endpoint

Through the native Langbase API, this operation is `GET v1/memory/:memoryName/documents` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-memory-documents.md) for the provider-specific parameters and requirements.

