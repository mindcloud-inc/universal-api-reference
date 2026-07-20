# WebScraper.IO: List Scraping Jobs

Lists scraping jobs in your WebScraper.IO organization.

```
GET https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/list-scraping-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/list-scraping-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/list-scraping-jobs?${params}`, {
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
| `sitemapId` | number | no | Filter jobs by sitemap ID. |
| `tag` | string | no | Filter jobs by tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customId": "string",
      "driver": "string",
      "id": 1,
      "jobsEmpty": 1,
      "jobsExecuted": 1,
      "jobsFailed": 1,
      "jobsNoValue": 1,
      "jobsScheduled": 1,
      "pageLoadDelay": 1,
      "requestInterval": 1,
      "scheduled": 1,
      "scrapingDuration": 1,
      "sitemapId": 1,
      "sitemapName": "Ava Chen",
      "status": "string",
      "storedRecordCount": 1,
      "testRun": 1,
      "timeCreated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customId` | string |  |
| `driver` | string |  |
| `id` | number |  |
| `jobsEmpty` | number |  |
| `jobsExecuted` | number |  |
| `jobsFailed` | number |  |
| `jobsNoValue` | number |  |
| `jobsScheduled` | number |  |
| `pageLoadDelay` | number |  |
| `requestInterval` | number |  |
| `scheduled` | number |  |
| `scrapingDuration` | number |  |
| `sitemapId` | number |  |
| `sitemapName` | string |  |
| `status` | string |  |
| `storedRecordCount` | number |  |
| `testRun` | number |  |
| `timeCreated` | number |  |

## Native endpoint

Through the native WebScraper.IO API, this operation is `GET /scraping-jobs` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scraping-jobs.md) for the provider-specific parameters and requirements.

