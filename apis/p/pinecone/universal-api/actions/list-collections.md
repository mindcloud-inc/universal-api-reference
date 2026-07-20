# Pinecone: List Collections

Retrieves collections for a Pinecone project.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-collections?${params}`, {
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
      "collections": [
        {
          "dimension": 1,
          "environment": "string",
          "name": "Ava Chen",
          "size": 1,
          "status": "string",
          "vector_count": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collections[].dimension` | number |  |
| `collections[].environment` | string |  |
| `collections[].name` | string |  |
| `collections[].size` | number |  |
| `collections[].status` | string |  |
| `collections[].vector_count` | number |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /collections` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

