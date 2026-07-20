# Pinecone: Rerank Results

Reranks search results with a Pinecone model.

```
POST https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/rerank-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/rerank-results" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "bge-reranker-v2-m3",
  "query": "What city is the capital of France?",
  "documents": "[object Object],[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/rerank-results', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "bge-reranker-v2-m3",
    "query": "What city is the capital of France?",
    "documents": "[object Object],[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | The reranking model to use. Example: `bge-reranker-v2-m3`. |
| `query` | string | yes | The query to rerank against. Example: `What city is the capital of France?`. |
| `documents` | list<object> | yes | The list of document objects to rerank. Pass an array like [{"text":"..."},{"text":"..."}]. Example: `[object Object],[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topN` | number | no | Optional number of top results to return. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "document": {
            "text": "string"
          },
          "index": 1,
          "score": 1
        }
      ],
      "model": "string",
      "usage": {
        "rerank_units": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].document.text` | string |  |
| `data[].index` | number |  |
| `data[].score` | number |  |
| `model` | string |  |
| `usage.rerank_units` | number |  |

## Native endpoint

Through the native Pinecone API, this operation is `POST /rerank` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rerank-results.md) for the provider-specific parameters and requirements.

