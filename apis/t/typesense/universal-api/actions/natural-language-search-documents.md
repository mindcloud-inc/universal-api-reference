# Typesense: Natural Language Search Documents

Finds documents in Typesense using natural language search.

```
GET https://connect.mindcloud.co/v1/universal/typesense/latest/actions/natural-language-search-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/natural-language-search-documents?connectionId=$CONNECTION_ID&collection=string&nlQuery=string&queryBy=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collection": "string",
  "nlQuery": "string",
  "queryBy": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/natural-language-search-documents?${params}`, {
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
| `nlQuery` | string | yes | Natural language search query. |
| `queryBy` | string | yes | Fields to search. |

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

Through the native Typesense API, this operation is `GET /collections/{{collection}}/documents/search` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/natural-language-search-documents.md) for the provider-specific parameters and requirements.

