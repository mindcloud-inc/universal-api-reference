# WebScraper.IO: Download Scraping Job CSV

Downloads scraping job data as CSV from WebScraper.IO.

```
GET https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/download-scraping-job-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/download-scraping-job-csv?connectionId=$CONNECTION_ID&scrapingJobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scrapingJobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/download-scraping-job-csv?${params}`, {
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
| `scrapingJobId` | number | yes | The Web Scraper scraping job ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `raw` | boolean | no | Return raw exported data when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | CSV export content. |

## Native endpoint

Through the native WebScraper.IO API, this operation is `GET /scraping-job/:scrapingJobId/csv` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-scraping-job-csv.md) for the provider-specific parameters and requirements.

