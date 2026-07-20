# WebScraper.IO: Get Sitemap Scheduler

Retrieves scheduler settings for a sitemap from WebScraper.IO.

```
GET https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-sitemap-scheduler
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-sitemap-scheduler?connectionId=$CONNECTION_ID&sitemapId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sitemapId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-sitemap-scheduler?${params}`, {
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
      "cronDay": "string",
      "cronHour": "string",
      "cronMinute": "string",
      "cronMonth": "string",
      "cronTimezone": "string",
      "cronWeekday": "string",
      "driver": "string",
      "pageLoadDelay": 1,
      "priority": 1,
      "proxy": "string",
      "requestInterval": 1,
      "schedulerEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cronDay` | string |  |
| `cronHour` | string |  |
| `cronMinute` | string |  |
| `cronMonth` | string |  |
| `cronTimezone` | string |  |
| `cronWeekday` | string |  |
| `driver` | string |  |
| `pageLoadDelay` | number |  |
| `priority` | number |  |
| `proxy` | string |  |
| `requestInterval` | number |  |
| `schedulerEnabled` | boolean |  |

## Native endpoint

Through the native WebScraper.IO API, this operation is `GET /sitemap/:sitemapId/scheduler` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sitemap-scheduler.md) for the provider-specific parameters and requirements.

