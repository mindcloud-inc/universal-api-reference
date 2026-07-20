# Tavily: Extract Content

Retrieves web page content from URLs with Tavily.

```
GET https://connect.mindcloud.co/v1/universal/tavily/latest/actions/extract-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tavily `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/extract-content?connectionId=$CONNECTION_ID&urls%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urls[]": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tavily/latest/actions/extract-content?${params}`, {
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
| `chunksPerSource` | number | no | Maximum number of relevant chunks to return per source when query is provided. |
| `extractDepth` | string | no | Extraction depth. Accepted values are basic or advanced. |
| `format` | string | no | Content format. Accepted values are markdown or text. |
| `includeFavicon` | boolean | no | Include the favicon URL for each result. |
| `includeImages` | boolean | no | Include extracted images in the response. |
| `includeUsage` | boolean | no | Include credit usage information in the response. |
| `query` | string | no | Optional user intent used to rerank extracted content chunks. |
| `timeout` | number | no | Maximum time in seconds to wait before timing out the extraction. |
| `urls[]` | array<string> | yes | One or more URLs to extract content from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed_results": [
        {}
      ],
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
| `failed_results` | array<object> | URLs that could not be processed. |
| `request_id` | string | Unique request identifier from Tavily. |
| `response_time` | number | Time in seconds it took to complete the request. |
| `results` | array<object> | Extracted content results for the requested URLs. |
| `usage` | object | Credit usage details for the request. |

## Native endpoint

Through the native Tavily API, this operation is `POST /extract` (base URL `https://api.tavily.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-content.md) for the provider-specific parameters and requirements.

