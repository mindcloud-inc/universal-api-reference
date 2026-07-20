# Vectara: Simple Single Corpus Query

Retrieves query results from a specific Vectara corpus.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/simple-single-corpus-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/simple-single-corpus-query?connectionId=$CONNECTION_ID&corpusKey=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "corpusKey": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/simple-single-corpus-query?${params}`, {
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
| `query` | string | yes | Question or search text to run against the corpus. |
| `limit` | number | no | Maximum number of results to return. |
| `offset` | number | no | Number of results to skip. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `saveHistory` | boolean | no | Whether to save this query in history. |
| `intelligentQueryRewriting` | boolean | no | Enable query rewriting and filter extraction improvements. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "factual_consistency_score": 1,
      "rendered_prompt": "string",
      "response_language": "string",
      "rewritten_queries": [
        {}
      ],
      "search_results": [
        {}
      ],
      "summary": "string",
      "warnings": [
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
| `factual_consistency_score` | number | Factual consistency score for the summary. |
| `rendered_prompt` | string | Rendered prompt sent to the LLM. |
| `response_language` | string | Response language. |
| `rewritten_queries` | array<object> | Rewritten queries generated for the request. |
| `search_results` | array<object> | Ranked search results. |
| `summary` | string | Summary of the query results. |
| `warnings` | array<string> | Non-fatal warnings from request processing. |

## Native endpoint

Through the native Vectara API, this operation is `GET /v2/corpora/:corpus_key/query` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/simple-single-corpus-query.md) for the provider-specific parameters and requirements.

