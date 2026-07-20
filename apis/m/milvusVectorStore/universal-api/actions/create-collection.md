# Milvus Vector Store: Create Collection

Creates a collection in Milvus Vector Store.

```
POST https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Milvus Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/create-collection', {
  method: 'POST',
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
| `data` | object | Created collection payload. |
| `message` | string | Provider message. |

## Native endpoint

Through the native Milvus Vector Store API, this operation is `POST /v2/vectordb/collections/create` (base URL `https://{{credentials.clusterEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

