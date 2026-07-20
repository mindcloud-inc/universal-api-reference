# Bolna: Create Knowledgebase from URL

Creates a new knowledgebase in Bolna from a URL.

```
POST https://connect.mindcloud.co/v1/universal/bolna/latest/actions/create-knowledgebase-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/create-knowledgebase-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bolna/latest/actions/create-knowledgebase-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL to ingest into the knowledgebase. |
| `chunkSize` | number | no | Chunk size for embedding model. Default: `512`. |
| `similarityTopK` | number | no | Number of top similar nodes to return. Default: `15`. |
| `overlapping` | number | no | Overlap between neighboring nodes. Default: `128`. |
| `languageSupport` | string | no | Enable multilingual retrieval mode. One of: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen",
      "languageSupport": "string",
      "ragId": "string",
      "sourceType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string |  |
| `languageSupport` | string |  |
| `ragId` | string |  |
| `sourceType` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bolna API, this operation is `POST /knowledgebase` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-knowledgebase-from-url.md) for the provider-specific parameters and requirements.

