# Vectara: Query Metadata

Queries metadata fields in a specific Vectara corpus.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/query-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/query-metadata?connectionId=$CONNECTION_ID&corpusKey=string&queries%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "corpusKey": "string",
  "queries[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/query-metadata?${params}`, {
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
| `corpusKey` | string | yes | Unique key of the corpus. |
| `queries[]` | array<object> | yes | Array of field-specific metadata queries to match. |
| `level` | list | no | Whether to search document-level or part-level metadata. One of: `0`, `1`. |
| `limit` | number | no | Maximum number of matched documents to return. |
| `offset` | number | no | Number of matching results to skip. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadataFilter` | string | no | Exact metadata filter applied before fuzzy matching. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> | Matched documents ordered by relevance score. |
| `total_count` | number | Total number of matching documents. |

## Native endpoint

Through the native Vectara API, this operation is `POST /v2/corpora/:corpus_key/metadata_query` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-metadata.md) for the provider-specific parameters and requirements.

