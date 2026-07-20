# WebScraper.IO: Get Scraping Job Problematic URLs

Retrieves problematic URLs for a scraping job from WebScraper.IO.

```
GET https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-scraping-job-problematic-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-scraping-job-problematic-urls?connectionId=$CONNECTION_ID&scrapingJobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scrapingJobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-scraping-job-problematic-urls?${params}`, {
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
| `page` | number | no | Page number to fetch. |
| `scrapingJobId` | number | yes | The Web Scraper scraping job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native WebScraper.IO API, this operation is `GET /scraping-job/:scrapingJobId/problematic-urls` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scraping-job-problematic-urls.md) for the provider-specific parameters and requirements.

