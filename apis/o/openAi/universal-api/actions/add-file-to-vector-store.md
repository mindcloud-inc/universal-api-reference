# Open AI: Add File To Vector Store

Adds a file to a vector store in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/add-file-to-vector-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/add-file-to-vector-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vector_store_id": "string",
  "file_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/add-file-to-vector-store', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vector_store_id": "string",
    "file_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vector_store_id` | string | yes | The ID of the vector store. |
| `file_id` | string | yes | The ID of the uploaded file to attach. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunkingStrategy": {
        "static": {
          "chunkOverlapTokens": 1,
          "maxChunkSizeTokens": 1
        },
        "type": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastError": {},
      "object": "string",
      "status": "string",
      "usageBytes": 1,
      "vectorStoreId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunkingStrategy.static.chunkOverlapTokens` | number |  |
| `chunkingStrategy.static.maxChunkSizeTokens` | number |  |
| `chunkingStrategy.type` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `lastError` | object |  |
| `object` | string |  |
| `status` | string |  |
| `usageBytes` | number |  |
| `vectorStoreId` | string |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/vector_stores/:vector_store_id/files` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-file-to-vector-store.md) for the provider-specific parameters and requirements.

