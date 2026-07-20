# Open AI: Delete Vector Store File

Deletes a vector store file from Open AI.

```
DELETE https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-vector-store-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-vector-store-file?connectionId=$CONNECTION_ID&file_id=file-9iKAYkbraQ7QHGmqhYnapo&vector_store_id=vs_69d92f86b7a48191ae62c4728fca7740" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "file-9iKAYkbraQ7QHGmqhYnapo",
  "vector_store_id": "vs_69d92f86b7a48191ae62c4728fca7740"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-vector-store-file?${params}`, {
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
| `file_id` | string | yes | Vector store file ID to delete. Default: `file-9iKAYkbraQ7QHGmqhYnapo`. |
| `vector_store_id` | string | yes | Vector store ID that owns the file. Default: `vs_69d92f86b7a48191ae62c4728fca7740`. |

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
| `deleted` | boolean | Whether the vector store file was deleted. |
| `id` | string | Deleted vector store file ID. |
| `object` | string | Object type. |

## Native endpoint

Through the native Open AI API, this operation is `DELETE v1/vector_stores/:vector_store_id/files/:file_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vector-store-file.md) for the provider-specific parameters and requirements.

