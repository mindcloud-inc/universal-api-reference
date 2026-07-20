# Open AI: Get Vector Store File Content

Retrieves vector store file contents from Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-vector-store-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-vector-store-file-content?connectionId=$CONNECTION_ID&file_id=file-9iKAYkbraQ7QHGmqhYnapo&vector_store_id=vs_69d92f86b7a48191ae62c4728fca7740" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "file-9iKAYkbraQ7QHGmqhYnapo",
  "vector_store_id": "vs_69d92f86b7a48191ae62c4728fca7740"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-vector-store-file-content?${params}`, {
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
| `file_id` | string | yes | Vector store file ID whose parsed contents to retrieve. Default: `file-9iKAYkbraQ7QHGmqhYnapo`. |
| `vector_store_id` | string | yes | Vector store ID that owns the file. Default: `vs_69d92f86b7a48191ae62c4728fca7740`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "content": [
        {
          "text": "string",
          "type": "string"
        }
      ],
      "file_id": "string",
      "filename": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | File attributes. |
| `content` | array<object> | Parsed file content blocks. |
| `content[].text` | string | Parsed text content. |
| `content[].type` | string | Content block type. |
| `file_id` | string | Vector store file ID. |
| `filename` | string | Filename. |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/vector_stores/:vector_store_id/files/:file_id/content` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vector-store-file-content.md) for the provider-specific parameters and requirements.

