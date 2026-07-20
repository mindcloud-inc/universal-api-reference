# FlowiseAI: Delete Document Store Chunk

Deletes a specific document chunk from FlowiseAI.

```
DELETE https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-chunk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-chunk?connectionId=$CONNECTION_ID&chunkId=string&loaderId=string&storeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chunkId": "string",
  "loaderId": "string",
  "storeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-chunk?${params}`, {
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
| `chunkId` | string | yes | Document store chunk ID to delete. |
| `loaderId` | string | yes | Document loader ID containing the chunk. |
| `storeId` | string | yes | Document store ID containing the chunk. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FlowiseAI API returns.

## Native endpoint

Through the native FlowiseAI API, this operation is `DELETE /document-store/chunks/{storeId}/{loaderId}/{chunkId}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document-store-chunk.md) for the provider-specific parameters and requirements.

