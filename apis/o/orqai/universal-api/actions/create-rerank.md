# Orq.ai: Create Rerank

Creates reranked search results in Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-rerank
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-rerank?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-rerank?${params}`, {
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
      "id": "string",
      "object": "string",
      "results": [
        {
          "document": {
            "text": "string"
          },
          "index": 1,
          "object": "string"
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
| `id` | string |  |
| `object` | string |  |
| `results[].document.text` | string |  |
| `results[].index` | number |  |
| `results[].object` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v2/router/rerank` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rerank.md) for the provider-specific parameters and requirements.

