# Hyperbrowser: Get Crawl Job Status and Results



```
GET https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-crawl-job-status-and-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperbrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-crawl-job-status-and-results?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-crawl-job-status-and-results?${params}`, {
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
| `id` | string | yes | Crawl job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchSize": 1,
      "currentPageBatch": 1,
      "data": [
        {}
      ],
      "error": "string",
      "jobId": "string",
      "status": "string",
      "totalCrawledPages": 1,
      "totalPageBatches": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchSize` | number |  |
| `currentPageBatch` | number |  |
| `data` | array<object> |  |
| `error` | string |  |
| `jobId` | string |  |
| `status` | string |  |
| `totalCrawledPages` | number |  |
| `totalPageBatches` | number |  |

## Native endpoint

Through the native Hyperbrowser API, this operation is `GET /api/crawl/:id` (base URL `https://api.hyperbrowser.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl-job-status-and-results.md) for the provider-specific parameters and requirements.

