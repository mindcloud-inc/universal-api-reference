# Milvus Vector Store: Upsert Vectors

Upserts vectors in Milvus Vector Store.

```
PUT https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/upsert-vectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Milvus Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/upsert-vectors" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/upsert-vectors', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
      "data": {},
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
| `data` | object | Upsert operation payload. |
| `message` | string | Provider message. |

## Native endpoint

Through the native Milvus Vector Store API, this operation is `POST /v2/vectordb/entities/upsert` (base URL `https://{{credentials.clusterEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-vectors.md) for the provider-specific parameters and requirements.

