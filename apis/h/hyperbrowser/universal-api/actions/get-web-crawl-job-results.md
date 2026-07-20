# Hyperbrowser: Get Web Crawl Job Results



```
GET https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-web-crawl-job-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperbrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-web-crawl-job-results?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-web-crawl-job-results?${params}`, {
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
| `id` | string | yes | Web crawl job identifier. |

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
      "jobId": "string",
      "status": "string",
      "totalPageBatches": 1,
      "totalPages": 1
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
| `jobId` | string |  |
| `status` | string |  |
| `totalPageBatches` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Hyperbrowser API, this operation is `GET /api/web/crawl/:id` (base URL `https://api.hyperbrowser.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-web-crawl-job-results.md) for the provider-specific parameters and requirements.

