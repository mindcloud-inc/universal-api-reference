# Milvus Vector Store: Search Vectors

Searches vectors in Milvus Vector Store.

```
GET https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/search-vectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Milvus Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/search-vectors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/search-vectors?${params}`, {
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
      "code": 1,
      "data": [
        {}
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Response code. |
| `data` | array<object> | Search hits. |
| `message` | string | Provider message. |

## Native endpoint

Through the native Milvus Vector Store API, this operation is `POST /v2/vectordb/entities/search` (base URL `https://{{credentials.clusterEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-vectors.md) for the provider-specific parameters and requirements.

