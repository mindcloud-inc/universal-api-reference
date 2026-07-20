# Firecrawl: Map Website

Retrieves website URLs from Firecrawl.

```
GET https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/map-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/map-website?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/map-website?${params}`, {
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
| `url` | string | yes | The base URL to start crawling from |
| `search` | string | no | Specify a search query to order the results by relevance |
| `sitemap` | string | no | Sitemap mode when mapping |
| `includeSubdomains` | boolean | no | Include subdomains of the website |
| `ignoreQueryParameters` | boolean | no | Do not return URLs with query parameters |
| `ignoreCache` | boolean | no | Bypass the sitemap cache to retrieve fresh URLs |
| `limit` | number | no | Maximum number of links to return |
| `timeout` | number | no | Timeout in milliseconds |
| `location` | object | no | Location settings for the request |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {
        "title": "https://example.com",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | array<object> |  |
| `links.title` | string |  |
| `links.url` | string |  |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /map` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/map-website.md) for the provider-specific parameters and requirements.

