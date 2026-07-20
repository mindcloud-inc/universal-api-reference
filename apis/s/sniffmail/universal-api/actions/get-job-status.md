# Sniffmail: Get Job Status

Retrieves the status of a bulk verification job.

```
GET https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sniffmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=job_abc123xyz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "job_abc123xyz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | Provide the Sniffmail bulk job ID returned by Create Bulk Job. Example: `job_abc123xyz`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "completedAt": "string",
        "createdAt": "string",
        "errorMessage": "string",
        "id": "string",
        "invalidEmails": 1,
        "processedEmails": 1,
        "progress": 1,
        "status": "string",
        "totalEmails": 1,
        "validEmails": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.completedAt` | string | When Sniffmail completed the bulk job, if available. |
| `job.createdAt` | string | When Sniffmail created the bulk job. |
| `job.errorMessage` | string | Any provider error message attached to the job. |
| `job.id` | string | The Sniffmail bulk job identifier. |
| `job.invalidEmails` | number | How many job emails Sniffmail classified as invalid. |
| `job.processedEmails` | number | How many email addresses Sniffmail has already processed. |
| `job.progress` | number | The reported completion percentage for the job. |
| `job.status` | string | The current bulk job status. |
| `job.totalEmails` | number | How many email addresses were submitted in the job. |
| `job.validEmails` | number | How many job emails Sniffmail classified as valid. |

## Native endpoint

Through the native Sniffmail API, this operation is `GET /jobs/:jobId` (base URL `https://api.sniffmail.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

