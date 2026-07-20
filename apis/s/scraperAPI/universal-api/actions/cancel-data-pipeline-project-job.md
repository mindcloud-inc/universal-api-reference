# ScraperAPI: Cancel DataPipeline Project Job

Cancels a DataPipeline project job in ScraperAPI.

```
DELETE https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/cancel-data-pipeline-project-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScraperAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/cancel-data-pipeline-project-job?connectionId=$CONNECTION_ID&id=1&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/cancel-data-pipeline-project-job?${params}`, {
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
| `id` | number | yes | The DataPipeline project ID. |
| `jobId` | string | yes | The DataPipeline job ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScraperAPI API returns.

## Native endpoint

Through the native ScraperAPI API, this operation is `DELETE https://datapipeline.scraperapi.com/api/projects/:id/jobs/:jobId` (base URL `https://api.scraperapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-data-pipeline-project-job.md) for the provider-specific parameters and requirements.

