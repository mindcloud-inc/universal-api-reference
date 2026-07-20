# Firecrawl: Scrape URL

Scrapes a single URL with Firecrawl.

```
GET https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/scrape-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/scrape-url?${params}`, {
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
| `url` | string | yes | The URL to scrape |
| `formats[]` | array<string> | no | Output formats to return |
| `onlyMainContent` | boolean | no | Return only the main page content |
| `includeTags[]` | array<string> | no | HTML tags to include in the output |
| `excludeTags[]` | array<string> | no | HTML tags to exclude from the output |
| `maxAge` | number | no | Maximum cache age in milliseconds |
| `headers` | object | no | Custom request headers for the target site |
| `waitFor` | number | no | Delay before scraping in milliseconds |
| `mobile` | boolean | no | Emulate a mobile device |
| `timeout` | number | no | Request timeout in milliseconds |
| `actions[]` | array<object> | no | Browser actions to run before scraping |
| `location` | object | no | Geo and language settings for the request |
| `removeBase64Images` | boolean | no | Replace embedded base64 images in markdown output |
| `blockAds` | boolean | no | Enable ad and cookie popup blocking |
| `proxy` | string | no | Proxy mode to use for scraping |
| `storeInCache` | boolean | no | Store the result in Firecrawl cache and index |
| `zeroDataRetention` | boolean | no | Enable zero data retention for this scrape |

## Response

```json
{
  "success": true,
  "data": [
    {
      "markdown": "string",
      "metadata": {
        "cachedAt": "2026-05-07T12:00:00.000Z",
        "cacheState": "string",
        "concurrencyLimited": true,
        "contentType": "string",
        "creditsUsed": 1,
        "language": "string",
        "proxyUsed": "string",
        "scrapeId": "string",
        "sourceURL": "https://example.com",
        "statusCode": 1,
        "title": "string",
        "url": "https://example.com",
        "viewport": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `markdown` | string | Markdown content extracted from the scraped page |
| `metadata.cachedAt` | date | When the cached result was created |
| `metadata.cacheState` | string | Firecrawl cache result state |
| `metadata.concurrencyLimited` | boolean | Whether Firecrawl concurrency limiting was applied |
| `metadata.contentType` | string | Response content type |
| `metadata.creditsUsed` | number | Credits consumed by the scrape |
| `metadata.language` | string | Detected page language |
| `metadata.proxyUsed` | string | Proxy tier used by Firecrawl |
| `metadata.scrapeId` | string | Firecrawl scrape job identifier |
| `metadata.sourceURL` | string | Original requested source URL |
| `metadata.statusCode` | number | HTTP status code returned by the source page |
| `metadata.title` | string | Page title |
| `metadata.url` | string | Final resolved page URL |
| `metadata.viewport` | string | Viewport metadata reported by the page |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /scrape` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url.md) for the provider-specific parameters and requirements.

