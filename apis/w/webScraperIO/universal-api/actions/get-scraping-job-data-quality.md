# WebScraper.IO: Get Scraping Job Data Quality

Retrieves data quality statistics for a WebScraper.IO scraping job.

```
GET https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-scraping-job-data-quality
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-scraping-job-data-quality?connectionId=$CONNECTION_ID&scrapingJobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scrapingJobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-scraping-job-data-quality?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "maxEmptyPagesPercent": {
        "expected": 1,
        "got": 1,
        "success": true
      },
      "maxFailedPagesPercent": {
        "expected": 1,
        "got": 1,
        "success": true
      },
      "maxNoValuePagesPercent": {
        "expected": 1,
        "got": 1,
        "success": true
      },
      "minColumnRecords": {
        "title": {
          "expected": 1,
          "got": 1,
          "success": true
        }
      },
      "minRecordCount": {
        "expected": 1,
        "got": 1,
        "success": true
      },
      "overallDataQualitySuccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `maxEmptyPagesPercent.expected` | number |  |
| `maxEmptyPagesPercent.got` | number |  |
| `maxEmptyPagesPercent.success` | boolean |  |
| `maxFailedPagesPercent.expected` | number |  |
| `maxFailedPagesPercent.got` | number |  |
| `maxFailedPagesPercent.success` | boolean |  |
| `maxNoValuePagesPercent.expected` | number |  |
| `maxNoValuePagesPercent.got` | number |  |
| `maxNoValuePagesPercent.success` | boolean |  |
| `minColumnRecords.title.expected` | number |  |
| `minColumnRecords.title.got` | number |  |
| `minColumnRecords.title.success` | boolean |  |
| `minRecordCount.expected` | number |  |
| `minRecordCount.got` | number |  |
| `minRecordCount.success` | boolean |  |
| `overallDataQualitySuccess` | boolean |  |

## Native endpoint

Through the native WebScraper.IO API, this operation is `GET /scraping-job/:scrapingJobId/data-quality` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scraping-job-data-quality.md) for the provider-specific parameters and requirements.

