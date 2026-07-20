# FlowiseAI: Delete Document Store Vector Store

Deletes vector store data from a FlowiseAI document store.

```
DELETE https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-vector-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-vector-store?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-vector-store?${params}`, {
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
| `id` | string | yes | Document store ID for vector store deletion. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FlowiseAI API returns.

## Native endpoint

Through the native FlowiseAI API, this operation is `DELETE /document-store/vectorstore/{id}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document-store-vector-store.md) for the provider-specific parameters and requirements.

