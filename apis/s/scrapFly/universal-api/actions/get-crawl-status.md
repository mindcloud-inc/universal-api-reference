# ScrapFly: Get Crawl Status

Retrieves crawl job status from ScrapFly.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/get-crawl-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/get-crawl-status?connectionId=$CONNECTION_ID&crawlerUuid=bf7282d8-818f-4a17-b3d7-a97a8f49ee65" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlerUuid": "bf7282d8-818f-4a17-b3d7-a97a8f49ee65"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/get-crawl-status?${params}`, {
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
| `crawlerUuid` | string | yes | Crawler job identifier returned when a crawl starts. Example: `bf7282d8-818f-4a17-b3d7-a97a8f49ee65`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "crawlerUuid": "string",
      "env": "string",
      "isFinished": true,
      "isSuccess": true,
      "project": "string",
      "state": {
        "apiCreditUsed": 1,
        "duration": 1,
        "startTime": 1,
        "stopReason": "string",
        "stopTime": 1,
        "urlsExtracted": 1,
        "urlsFailed": 1,
        "urlsSkipped": 1,
        "urlsToCrawl": 1,
        "urlsVisited": 1
      },
      "status": "string",
      "urls": {},
      "userUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `crawlerUuid` | string | Crawler UUID. |
| `env` | string | ScrapFly environment. |
| `isFinished` | boolean | Whether the crawl has finished. |
| `isSuccess` | boolean | Whether the crawl completed successfully. |
| `project` | string | ScrapFly project name. |
| `state.apiCreditUsed` | number | API credits used by the crawl. |
| `state.duration` | number | Crawl duration in seconds. |
| `state.startTime` | number | Unix start time. |
| `state.stopReason` | string | Why the crawl stopped. |
| `state.stopTime` | number | Unix stop time. |
| `state.urlsExtracted` | number | Number of extracted URLs. |
| `state.urlsFailed` | number | Number of failed URLs. |
| `state.urlsSkipped` | number | Number of skipped URLs. |
| `state.urlsToCrawl` | number | Number of queued URLs. |
| `state.urlsVisited` | number | Number of visited URLs. |
| `status` | string | Crawler status. |
| `urls` | object | Map of crawled URLs to crawl states. |
| `userUuid` | string | ScrapFly user UUID. |

## Native endpoint

Through the native ScrapFly API, this operation is `GET /crawl/:crawlerUuid/status` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl-status.md) for the provider-specific parameters and requirements.

