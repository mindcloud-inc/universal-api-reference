# Firecrawl: Batch Scrape URLs

Creates a batch scrape job in Firecrawl.

```
POST https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/batch-scrape-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/batch-scrape-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/batch-scrape-urls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls[]` | array<string> | yes | The URLs to scrape |
| `formats[]` | array<string> | no | Output formats to return for each scraped URL |
| `onlyMainContent` | boolean | no | Return only the main content of each page |
| `includeTags[]` | array<string> | no | HTML tags to include in the output |
| `excludeTags[]` | array<string> | no | HTML tags to exclude from the output |
| `maxAge` | number | no | Maximum cache age in milliseconds |
| `minAge` | number | no | Minimum cache age in milliseconds for cache-only reads |
| `headers` | object | no | Custom request headers for the target sites |
| `waitFor` | number | no | Delay before scraping in milliseconds |
| `mobile` | boolean | no | Emulate a mobile device |
| `skipTlsVerification` | boolean | no | Skip TLS certificate verification when making requests |
| `timeout` | number | no | Request timeout in milliseconds |
| `parsers[]` | array<object> | no | File parsing controls for supported file types |
| `actions[]` | array<object> | no | Browser actions to run before scraping each page |
| `location` | object | no | Geo and language settings for the request |
| `removeBase64Images` | boolean | no | Replace embedded base64 images in markdown output |
| `blockAds` | boolean | no | Enable ad and cookie popup blocking |
| `proxy` | string | no | Proxy mode to use for scraping |
| `storeInCache` | boolean | no | Store the scraped pages in Firecrawl cache and index |
| `webhook` | object | no | Webhook specification for batch scrape events |
| `maxConcurrency` | number | no | Maximum number of concurrent scrapes |
| `ignoreInvalidURLs` | boolean | no | Ignore invalid URLs instead of failing the entire request |
| `zeroDataRetention` | boolean | no | Enable zero data retention for this batch scrape |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "invalidURLs": [
        "https://example.com"
      ],
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
| `invalidURLs` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /batch/scrape` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-scrape-urls.md) for the provider-specific parameters and requirements.

