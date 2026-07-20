# Typesense: Vector Search Documents

Finds documents in Typesense using vector search.

```
GET https://connect.mindcloud.co/v1/universal/typesense/latest/actions/vector-search-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/vector-search-documents?connectionId=$CONNECTION_ID&collection=string&q=*&queryBy=string&vectorQuery=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collection": "string",
  "q": "*",
  "queryBy": "string",
  "vectorQuery": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/vector-search-documents?${params}`, {
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
| `collection` | string | yes | Collection name. |
| `q` | string | yes | Text query, often * for vector-only search. Default: `*`. |
| `queryBy` | string | yes | Fields to search. |
| `vectorQuery` | string | yes | Typesense vector_query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "found": 1,
      "hits": [
        {}
      ],
      "out_of": 1,
      "response": {},
      "search_time_ms": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `found` | number |  |
| `hits` | array<object> |  |
| `out_of` | number |  |
| `response` | object |  |
| `search_time_ms` | number |  |

## Native endpoint

Through the native Typesense API, this operation is `GET /collections/{{collection}}/documents/search` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vector-search-documents.md) for the provider-specific parameters and requirements.

