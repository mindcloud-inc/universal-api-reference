# Open AI: Delete Vector Store

Deletes a vector store from Open AI.

```
DELETE https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-vector-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-vector-store?connectionId=$CONNECTION_ID&vector_store_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vector_store_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-vector-store?${params}`, {
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
| `vector_store_id` | string | yes | Vector store ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the vector store was deleted. |
| `id` | string | Deleted vector store ID. |
| `object` | string | Object type. |

## Native endpoint

Through the native Open AI API, this operation is `DELETE v1/vector_stores/:vector_store_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vector-store.md) for the provider-specific parameters and requirements.

