# Cloudflare Browser Run: Cancel Crawl Job

Cancels a crawl job in Cloudflare Browser Run.

```
DELETE https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/cancel-crawl-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/cancel-crawl-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/cancel-crawl-job?${params}`, {
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
| `jobId` | string | yes | Crawl job ID to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "job_id": "string",
        "message": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.job_id` | string |  |
| `result.message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `DELETE /accounts/:accountId/browser-rendering/crawl/:jobId` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-crawl-job.md) for the provider-specific parameters and requirements.

