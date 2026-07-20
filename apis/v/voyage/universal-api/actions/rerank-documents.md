# Voyage: Rerank Documents

Reranks documents in Voyage for a query.

```
POST https://connect.mindcloud.co/v1/universal/voyage/latest/actions/rerank-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voyage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/rerank-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string",
  "documents[]": [
    "string"
  ],
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voyage/latest/actions/rerank-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string",
    "documents[]": ["string"],
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Query text used to rerank documents. |
| `documents[]` | array<string> | yes | Documents to rerank. |
| `model` | string | yes | Reranker model to use. |
| `topK` | number | no | Maximum number of reranked documents to return. |
| `returnDocuments` | boolean | no | Whether to include documents in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document": "string",
      "index": 1,
      "relevance_score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document` | string | Document text when return_documents is enabled. |
| `index` | number | Zero-based index of the document in the request. |
| `relevance_score` | number | Voyage relevance score for the ranked document. |

## Native endpoint

Through the native Voyage API, this operation is `POST /v1/rerank` (base URL `https://api.voyageai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rerank-documents.md) for the provider-specific parameters and requirements.

