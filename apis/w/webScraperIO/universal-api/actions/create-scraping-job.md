# WebScraper.IO: Create Scraping Job

Creates a new scraping job in WebScraper.IO.

```
POST https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/create-scraping-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/create-scraping-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driver": "string",
  "pageLoadDelay": 1,
  "proxy": "string",
  "requestInterval": 1,
  "sitemapId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/create-scraping-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `customId` | string | no | Optional custom identifier included in notifications. |
| `driver` | string | yes | Scraping driver: fast or fulljs. |
| `pageLoadDelay` | number | yes | Delay after page load in milliseconds. |
| `proxy` | string | yes | Proxy region code. |
| `requestInterval` | number | yes | Delay between requests in milliseconds. |
| `sitemapId` | number | yes | The sitemap to scrape. |
| `startUrls[]` | array<string> | no | Optional start URLs override for the job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customId": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customId` | string |  |
| `id` | number |  |

## Native endpoint

Through the native WebScraper.IO API, this operation is `POST /scraping-job` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scraping-job.md) for the provider-specific parameters and requirements.

