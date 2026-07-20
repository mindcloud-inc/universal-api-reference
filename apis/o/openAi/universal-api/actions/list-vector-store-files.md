# Open AI: List Vector Store Files

Retrieves vector store files from Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-vector-store-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-vector-store-files?connectionId=$CONNECTION_ID&vector_store_id=vs_69d92f86b7a48191ae62c4728fca7740" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vector_store_id": "vs_69d92f86b7a48191ae62c4728fca7740"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-vector-store-files?${params}`, {
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
| `vector_store_id` | string | yes | Vector store ID whose files to list. Default: `vs_69d92f86b7a48191ae62c4728fca7740`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string",
          "object": "string",
          "status": "string",
          "usage_bytes": 1,
          "vector_store_id": "string"
        }
      ],
      "first_id": "string",
      "has_more": true,
      "last_id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned vector store files. |
| `data[].id` | string | Vector store file ID. |
| `data[].object` | string | Object type. |
| `data[].status` | string | Indexing status. |
| `data[].usage_bytes` | number | Storage usage in bytes. |
| `data[].vector_store_id` | string | Owning vector store ID. |
| `first_id` | string | First returned file ID. |
| `has_more` | boolean | Whether more files are available. |
| `last_id` | string | Last returned file ID. |
| `object` | string | List object type. |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/vector_stores/:vector_store_id/files` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vector-store-files.md) for the provider-specific parameters and requirements.

