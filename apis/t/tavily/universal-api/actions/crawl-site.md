# Tavily: Crawl Site

Crawls a website from a base URL with Tavily.

```
GET https://connect.mindcloud.co/v1/universal/tavily/latest/actions/crawl-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tavily `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/crawl-site?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tavily/latest/actions/crawl-site?${params}`, {
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
| `allowExternal` | boolean | no | Whether to include external domain links in the results. |
| `chunksPerSource` | number | no | Maximum number of relevant chunks to return per source when instructions are provided. |
| `excludeDomains[]` | array<string> | no | Regex patterns to exclude specific domains or subdomains. |
| `excludePaths[]` | array<string> | no | Regex patterns to exclude specific URL paths. |
| `extractDepth` | string | no | Extraction depth. Accepted values are basic or advanced. |
| `format` | string | no | Content format. Accepted values are markdown or text. |
| `includeFavicon` | boolean | no | Whether to include the favicon URL for each result. |
| `includeImages` | boolean | no | Whether to include images in the crawl results. |
| `includeUsage` | boolean | no | Include credit usage information in the response. |
| `instructions` | string | no | Natural language instructions for the crawler. |
| `limit` | number | no | Total number of links the crawler will process before stopping. |
| `maxBreadth` | number | no | Max number of links to follow per page. |
| `maxDepth` | number | no | Max depth of the crawl from the root URL. |
| `selectDomains[]` | array<string> | no | Regex patterns to include only specific domains or subdomains. |
| `selectPaths[]` | array<string> | no | Regex patterns to include only specific URL paths. |
| `timeout` | number | no | Maximum time in seconds to wait for the crawl operation before timing out. |
| `url` | string | yes | The root URL to begin the crawl. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_url": "https://example.com",
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
| `base_url` | string | The base URL that was crawled. |
| `request_id` | string | Unique request identifier from Tavily. |
| `response_time` | number | Time in seconds it took to complete the request. |
| `results` | array<object> | Extracted content from the crawled URLs. |
| `usage` | object | Credit usage details for the request. |

## Native endpoint

Through the native Tavily API, this operation is `POST /crawl` (base URL `https://api.tavily.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crawl-site.md) for the provider-specific parameters and requirements.

