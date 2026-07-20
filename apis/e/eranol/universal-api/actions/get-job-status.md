# Eranol: Get Job Status

Retrieves the status of an Eranol job.

```
GET https://connect.mindcloud.co/v1/universal/eranol/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eranol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/get-job-status?connectionId=$CONNECTION_ID&job_id=460719d5-d0ad-4fd8-a81c-ebc2435fbfaa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_id": "460719d5-d0ad-4fd8-a81c-ebc2435fbfaa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eranol/latest/actions/get-job-status?${params}`, {
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
| `job_id` | string | yes | Job ID returned by an Eranol create action. Example: `460719d5-d0ad-4fd8-a81c-ebc2435fbfaa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": 1,
      "createdAt": 1,
      "jobId": "string",
      "jobType": "string",
      "progress": 1,
      "result": {},
      "startedAt": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | number | Job completion time as a Unix timestamp. |
| `createdAt` | number | Job creation time as a Unix timestamp. |
| `jobId` | string | Unique Eranol job identifier. |
| `jobType` | string | Provider job type label. |
| `progress` | number | Provider-reported job progress when available. |
| `result` | object | Completed job result summary. |
| `startedAt` | number | Job start time as a Unix timestamp. |
| `status` | string | Current job state. |

## Native endpoint

Through the native Eranol API, this operation is `GET /ffmpeg/status/:job_id` (base URL `https://eranol.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

