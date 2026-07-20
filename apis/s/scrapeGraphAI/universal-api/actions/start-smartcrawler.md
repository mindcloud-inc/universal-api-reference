# ScrapeGraphAI: Start SmartCrawler

Starts a SmartCrawler crawl job in ScrapeGraphAI.

```
POST https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-smartcrawler
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-smartcrawler" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://scrapegraphai.com/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-smartcrawler', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://scrapegraphai.com/"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `depth` | number | no | Maximum crawl depth. Default: `1`. Example: `1`. |
| `maxPages` | number | no | Maximum number of pages to crawl. Default: `10`. Example: `1`. |
| `url` | string | yes | Starting URL for the crawl. Example: `https://scrapegraphai.com/`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchSize` | number | no | Number of pages to process in each batch. Default: `1`. Example: `1`. |
| `breadth` | number | no | Maximum number of links to crawl per depth level. Example: `5`. |
| `cacheWebsite` | boolean | no | Whether to cache website content. Default: `false`. |
| `extractionMode` | boolean | no | When false, use markdown conversion mode instead of AI extraction. Default: `true`. |
| `prompt` | string | no | Extraction instructions, required when Extraction Mode is true. Example: `Extract all visible page titles and summaries`. |
| `rules` | object | no | Optional crawl rules object for include and exclude logic. Example: `[object Object]`. |
| `sameDomainOnly` | boolean | no | Restrict crawling to the same domain. Default: `true`. |
| `schema` | object | no | Optional JSON schema object for structured extraction output. Example: `[object Object]`. |
| `sitemap` | boolean | no | Use sitemap.xml for discovery. Default: `false`. |
| `stealth` | boolean | no | Enable stealth mode to bypass bot protection. Default: `false`. |
| `waitMs` | number | no | Milliseconds to wait before scraping each page. Default: `3000`. Example: `3000`. |
| `webhookUrl` | string | no | Webhook URL to receive completion notifications. Example: `https://example.com/webhook`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string | Unique identifier for the SmartCrawler task. |

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `POST /crawl` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-smartcrawler.md) for the provider-specific parameters and requirements.

