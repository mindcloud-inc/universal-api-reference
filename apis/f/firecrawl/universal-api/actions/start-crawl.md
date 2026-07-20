# Firecrawl: Start Crawl

Creates a crawl job in Firecrawl.

```
POST https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/start-crawl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/start-crawl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/start-crawl', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The base URL to start crawling from |
| `prompt` | string | no | Prompt to generate crawler options from natural language |
| `excludePaths[]` | array<string> | no | URL pathname regex patterns to exclude from the crawl |
| `includePaths[]` | array<string> | no | URL pathname regex patterns to include in the crawl |
| `maxDiscoveryDepth` | number | no | Maximum discovery depth to crawl |
| `sitemap` | string | no | Sitemap mode when crawling |
| `ignoreQueryParameters` | boolean | no | Do not re-scrape the same path with different query parameters |
| `regexOnFullURL` | boolean | no | Match include and exclude regexes against the full URL |
| `limit` | number | no | Maximum number of pages to crawl |
| `crawlEntireDomain` | boolean | no | Allow crawling internal sibling and parent URLs |
| `allowExternalLinks` | boolean | no | Allow the crawler to follow external links |
| `allowSubdomains` | boolean | no | Allow the crawler to follow subdomain links |
| `delay` | number | no | Delay in seconds between scrapes |
| `maxConcurrency` | number | no | Maximum number of concurrent scrapes |
| `webhook` | object | no | Webhook specification for crawl events |
| `scrapeOptions` | object | no | Scrape options to apply to each crawled page |
| `zeroDataRetention` | boolean | no | Enable zero data retention for this crawl |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /crawl` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-crawl.md) for the provider-specific parameters and requirements.

