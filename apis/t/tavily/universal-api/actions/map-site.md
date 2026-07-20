# Tavily: Map Site

Maps a website from a base URL with Tavily.

```
GET https://connect.mindcloud.co/v1/universal/tavily/latest/actions/map-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tavily `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/map-site?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tavily/latest/actions/map-site?${params}`, {
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
| `allowExternal` | boolean | no | Whether to include external domain links in the discovered URLs. |
| `excludeDomains[]` | array<string> | no | Regex patterns to exclude specific domains or subdomains. |
| `excludePaths[]` | array<string> | no | Regex patterns to exclude specific URL paths. |
| `includeUsage` | boolean | no | Include credit usage information in the response. |
| `limit` | number | no | Total number of links the mapper will process before stopping. |
| `maxBreadth` | number | no | Max number of links to follow per page. |
| `maxDepth` | number | no | Max depth of the mapping from the root URL. |
| `selectDomains[]` | array<string> | no | Regex patterns to include only specific domains or subdomains. |
| `selectPaths[]` | array<string> | no | Regex patterns to include only specific URL paths. |
| `timeout` | number | no | Maximum time in seconds to wait for the map operation before timing out. |
| `url` | string | yes | The root URL to begin the site map discovery. |

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
        "string"
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
| `base_url` | string | The base URL that was mapped. |
| `request_id` | string | Unique request identifier from Tavily. |
| `response_time` | number | Time in seconds it took to complete the request. |
| `results` | array<string> | URLs discovered during the site map operation. |
| `usage` | object | Credit usage details for the request. |

## Native endpoint

Through the native Tavily API, this operation is `POST /map` (base URL `https://api.tavily.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/map-site.md) for the provider-specific parameters and requirements.

