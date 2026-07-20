# Open AI: Search Vector Store

Searches a vector store in Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/search-vector-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/search-vector-store?connectionId=$CONNECTION_ID&vector_store_id=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vector_store_id": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/search-vector-store?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vector_store_id` | string | yes | The ID of the vector store to search. |
| `query` | string | yes | Natural language query used for semantic search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "nextPage": {},
      "object": "string",
      "searchQuery": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `nextPage` | object |  |
| `object` | string |  |
| `searchQuery[]` | string |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/vector_stores/:vector_store_id/search` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-vector-store.md) for the provider-specific parameters and requirements.

