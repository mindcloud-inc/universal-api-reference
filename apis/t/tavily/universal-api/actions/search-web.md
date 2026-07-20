# Tavily: Search Web

Finds web search results in Tavily by query.

```
GET https://connect.mindcloud.co/v1/universal/tavily/latest/actions/search-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tavily `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/search-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tavily/latest/actions/search-web?${params}`, {
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
| `chunksPerSource` | number | no | The maximum number of relevant content chunks to return per source when search depth is advanced. |
| `country` | string | no | Prioritize search results from a specific country when topic is general. |
| `endDate` | date | no | Return results before this date in YYYY-MM-DD format. |
| `excludeDomains[]` | array<string> | no | A list of domains to specifically exclude from the search results. |
| `includeAnswer` | string | no | Include an LLM-generated answer. Accepted values are false, true, basic, or advanced. |
| `includeDomains[]` | array<string> | no | A list of domains to specifically include in the search results. |
| `includeImageDescriptions` | boolean | no | When include images is true, also return a description for each image. |
| `includeRawContent` | string | no | Include cleaned HTML content from each result. Accepted values are false, true, markdown, or text. |
| `query` | string | yes | The search query to execute with Tavily. |
| `startDate` | date | no | Return results after this date in YYYY-MM-DD format. |
| `timeout` | number | no | Maximum time in seconds to wait for the search request. |
| `timeRange` | string | no | The time range back from the current date to filter results by publish or update date. |
| `searchDepth` | string | no | Controls the latency versus relevance tradeoff for the search. |
| `topic` | string | no | The category of the search. |
| `maxResults` | number | no | The maximum number of search results to return. |
| `includeImages` | boolean | no | Also perform an image search and include image results. |
| `includeFavicon` | boolean | no | Include favicon URLs for each result when available. |
| `autoParameters` | boolean | no | Automatically configure search parameters based on the query intent. |
| `exactMatch` | boolean | no | Return only results containing the quoted exact phrase. |
| `includeUsage` | boolean | no | Include credit usage information in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "auto_parameters": {},
      "follow_up_questions": [
        "string"
      ],
      "images": [
        {}
      ],
      "query": "string",
      "request_id": "string",
      "response_time": 1,
      "results": [
        {}
      ],
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | LLM-generated answer when include_answer is requested. |
| `auto_parameters` | object | Auto-selected search parameters when auto_parameters is enabled. |
| `follow_up_questions` | array<string> | Suggested follow-up questions when provided by Tavily. |
| `images` | array<object> | Image search results when include_images is enabled. |
| `query` | string | The search query that was executed. |
| `request_id` | string | Unique request identifier from Tavily. |
| `response_time` | number | Time in seconds it took to complete the request. |
| `results` | array<object> | Ranked search results returned by Tavily. |
| `usage` | object | Credit usage details for the request. |

## Native endpoint

Through the native Tavily API, this operation is `POST /search` (base URL `https://api.tavily.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-web.md) for the provider-specific parameters and requirements.

