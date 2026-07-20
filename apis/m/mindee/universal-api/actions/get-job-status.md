# Mindee: Get Job Status

Retrieves a job status from Mindee.

```
GET https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mindee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | UUID of the job to retrieve |
| `redirect` | boolean | no | Automatically redirect to the result URL Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "completed_at": "2026-05-07T12:00:00.000Z",
        "created_at": "2026-05-07T12:00:00.000Z",
        "filename": "Ava Chen",
        "id": "string",
        "model_id": "string",
        "polling_url": "https://example.com",
        "result_url": "https://example.com",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.completed_at` | date |  |
| `job.created_at` | date |  |
| `job.filename` | string |  |
| `job.id` | string |  |
| `job.model_id` | string |  |
| `job.polling_url` | string |  |
| `job.result_url` | string |  |
| `job.status` | string |  |

## Native endpoint

Through the native Mindee API, this operation is `GET /v2/jobs/:job_id` (base URL `https://api-v2.mindee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

