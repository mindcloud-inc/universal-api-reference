# Vectara: Multi Corpora Query

Retrieves query results across multiple Vectara corpora.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/multi-corpora-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/multi-corpora-query?connectionId=$CONNECTION_ID&query=string&search.corpora%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "search.corpora[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/multi-corpora-query?${params}`, {
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
| `query` | string | yes | Question or search text to run across one or more corpora. |
| `search.corpora[]` | array<object> | yes | Array of corpus search objects with corpus_key and optional per-corpus settings. |
| `search.limit` | number | no | Maximum number of results to retrieve before reranking. |
| `search.offset` | number | no | Number of search results to skip. |
| `generation.generationPresetName` | string | no | Generation preset to use for grounded generation. |
| `generation.maxUsedSearchResults` | number | no | Maximum number of top search results sent to generation. |
| `generation.responseLanguage` | string | no | Language code for the generated response. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search.contextConfiguration` | object | no | Context window configuration for each search result. |
| `search.reranker` | object | no | Reranker configuration object. |
| `generation.promptTemplate` | string | no | Optional custom prompt template for generation. |
| `generation.modelParameters` | object | no | Optional model parameter overrides for generation. |
| `generation.citations` | object | no | Citation formatting configuration. |
| `generation.enableFactualConsistencyScore` | boolean | no | Whether to include a factual consistency score. |
| `streamResponse` | boolean | no | Whether to stream the query response. |
| `saveHistory` | boolean | no | Whether to save this query in history. |
| `intelligentQueryRewriting` | boolean | no | Enable query rewriting and metadata filter extraction. |

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

Through the native Vectara API, this operation is `POST /v2/query` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/multi-corpora-query.md) for the provider-specific parameters and requirements.

