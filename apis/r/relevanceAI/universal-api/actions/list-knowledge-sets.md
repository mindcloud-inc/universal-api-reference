# Relevance AI: List Knowledge Sets



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-knowledge-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-knowledge-sets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-knowledge-sets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "knowledge_chunked_count": 1,
      "knowledge_count": 1,
      "knowledge_set": "string",
      "knowledge_vectorized_count": 1,
      "metadata": {
        "description": "string",
        "model": "string",
        "vectorizing_info": {
          "status": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `knowledge_chunked_count` | number | The number of chunked rows. |
| `knowledge_count` | number | The number of knowledge rows. |
| `knowledge_set` | string | The knowledge set name. |
| `knowledge_vectorized_count` | number | The number of vectorized rows. |
| `metadata.description` | string | The knowledge set description. |
| `metadata.model` | string | The embedding model. |
| `metadata.vectorizing_info.status` | string | The vectorization status. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /knowledge/sets/list` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-knowledge-sets.md) for the provider-specific parameters and requirements.

