# Open AI Universal API Examples

These examples use the MindCloud API key and Open AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves available models from Open AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-models?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "object": "string",
          "ownedBy": "string"
        }
      ],
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openAi/latest/actions/list-models).

## Add File To Vector Store

Adds a file to a vector store in Open AI.

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

Example response:

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

See the full [Add File To Vector Store action reference](actions/add-file-to-vector-store.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openAi/latest/actions/add-file-to-vector-store).
