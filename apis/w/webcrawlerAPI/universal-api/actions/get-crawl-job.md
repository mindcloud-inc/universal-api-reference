# Webcrawler API: Get Crawl Job

Retrieves crawl job status and results from Webcrawler API.

```
GET https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-crawl-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-crawl-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-crawl-job?${params}`, {
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
| `id` | string | yes | Crawl job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowSubdomains": true,
      "blacklistRegexp": "string",
      "crawlerId": "string",
      "createdAt": "string",
      "finishedAt": "string",
      "id": "string",
      "itemsLimit": 1,
      "jobItems": [
        {}
      ],
      "maxDepth": 1,
      "orgId": "string",
      "recommendedPullDelayMs": 1,
      "respectRobotsTxt": true,
      "scrapeType": "string",
      "status": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "webhookUrl": "https://example.com",
      "whitelistRegexp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowSubdomains` | boolean | Whether subdomains are included in the crawl when configured. |
| `blacklistRegexp` | string | Optional exclusion pattern applied to crawled URLs. |
| `crawlerId` | string | Provider crawler identifier when returned. |
| `createdAt` | string | Creation timestamp for the crawl job. |
| `finishedAt` | string | Completion timestamp for the crawl job when available. |
| `id` | string | Crawl job identifier. |
| `itemsLimit` | number | Configured item limit for the crawl. |
| `jobItems` | array<object> | Per-page crawl item results returned by the provider. |
| `maxDepth` | number | Configured crawl depth. |
| `orgId` | string | Organization identifier that owns the crawl job. |
| `recommendedPullDelayMs` | number | Suggested delay before polling the job again. |
| `respectRobotsTxt` | boolean | Whether the crawl respects robots.txt. |
| `scrapeType` | string | Configured crawl output format. |
| `status` | string | Current crawl job status. |
| `updatedAt` | string | Last update timestamp for the crawl job. |
| `url` | string | Root URL for the crawl job. |
| `webhookUrl` | string | Optional webhook URL configured for the crawl job. |
| `whitelistRegexp` | string | Optional inclusion pattern applied to crawled URLs. |

## Native endpoint

Through the native Webcrawler API API, this operation is `GET /v1/job/:id` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl-job.md) for the provider-specific parameters and requirements.

