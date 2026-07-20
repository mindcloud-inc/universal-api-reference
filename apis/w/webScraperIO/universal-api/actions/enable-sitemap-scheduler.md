# WebScraper.IO: Enable Sitemap Scheduler

Enables scheduler settings for a sitemap in WebScraper.IO.

```
PUT https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/enable-sitemap-scheduler
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/enable-sitemap-scheduler" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cronDay": "string",
  "cronHour": "string",
  "cronMinute": "string",
  "cronMonth": "string",
  "cronTimezone": "string",
  "cronWeekday": "string",
  "driver": "string",
  "pageLoadDelay": 1,
  "proxy": "string",
  "requestInterval": 1,
  "sitemapId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/enable-sitemap-scheduler', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cronDay": "string",
    "cronHour": "string",
    "cronMinute": "string",
    "cronMonth": "string",
    "cronTimezone": "string",
    "cronWeekday": "string",
    "driver": "string",
    "pageLoadDelay": 1,
    "proxy": "string",
    "requestInterval": 1,
    "sitemapId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cronDay` | string | yes | Cron day-of-month expression. |
| `cronHour` | string | yes | Cron hour expression. |
| `cronMinute` | string | yes | Cron minute expression. |
| `cronMonth` | string | yes | Cron month expression. |
| `cronTimezone` | string | yes | Timezone for the cron schedule. |
| `cronWeekday` | string | yes | Cron weekday expression. |
| `driver` | string | yes | Scraping driver: fast or fulljs. |
| `pageLoadDelay` | number | yes | Delay after page load in milliseconds. |
| `proxy` | string | yes | Proxy region code. |
| `requestInterval` | number | yes | Delay between requests in milliseconds. |
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

Through the native WebScraper.IO API, this operation is `POST /sitemap/:sitemapId/enable-scheduler` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-sitemap-scheduler.md) for the provider-specific parameters and requirements.

