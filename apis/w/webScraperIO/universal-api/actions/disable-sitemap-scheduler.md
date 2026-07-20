# WebScraper.IO: Disable Sitemap Scheduler

Disables scheduler settings for a sitemap in WebScraper.IO.

```
DELETE https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/disable-sitemap-scheduler
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/disable-sitemap-scheduler?connectionId=$CONNECTION_ID&sitemapId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sitemapId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/disable-sitemap-scheduler?${params}`, {
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
| `sitemapId` | number | yes | The Web Scraper sitemap ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native WebScraper.IO API, this operation is `POST /sitemap/:sitemapId/disable-scheduler` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-sitemap-scheduler.md) for the provider-specific parameters and requirements.

