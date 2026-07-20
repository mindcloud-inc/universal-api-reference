# Cohere: Rerank

Reranks documents in Cohere for a search query.

```
GET https://connect.mindcloud.co/v1/universal/cohere/latest/actions/rerank
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/rerank?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/rerank?${params}`, {
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
      "meta": {},
      "results": [
        {}
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
| `meta` | object |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Cohere API, this operation is `POST /v1/rerank` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rerank.md) for the provider-specific parameters and requirements.

