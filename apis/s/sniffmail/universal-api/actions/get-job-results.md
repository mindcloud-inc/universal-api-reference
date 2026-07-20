# Sniffmail: Get Job Results

Retrieves results for a bulk verification job.

```
GET https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/get-job-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sniffmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/get-job-results?connectionId=$CONNECTION_ID&jobId=job_abc123xyz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "job_abc123xyz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/get-job-results?${params}`, {
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
        "id": "string",
        "invalidEmails": 1,
        "processedEmails": 1,
        "status": "string",
        "totalEmails": 1,
        "validEmails": 1
      },
      "results": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.completedAt` | string | When Sniffmail completed the bulk job. |
| `job.createdAt` | string | When Sniffmail created the bulk job. |
| `job.id` | string | The Sniffmail bulk job identifier. |
| `job.invalidEmails` | number | How many job emails Sniffmail classified as invalid. |
| `job.processedEmails` | number | How many email addresses Sniffmail processed. |
| `job.status` | string | The final or current job status. |
| `job.totalEmails` | number | How many email addresses were submitted in the job. |
| `job.validEmails` | number | How many job emails Sniffmail classified as valid. |
| `results[]` | array<object> | The per-email verification results returned for the bulk job. |
| `results[].deliverabilityScore` | number | The provider deliverability score for the email result. |
| `results[].disposable` | boolean | Whether Sniffmail classified the address as disposable. |
| `results[].email` | string | The email address Sniffmail evaluated. |
| `results[].freeProvider` | boolean | Whether Sniffmail classified the domain as a free email provider. |
| `results[].mxRecords` | boolean | Whether the domain has MX records according to Sniffmail. |
| `results[].reason` | string | The provider reason associated with the email result. |
| `results[].result` | string | The provider classification for the email result. |
| `results[].roleAccount` | boolean | Whether Sniffmail classified the address as a role account. |

## Native endpoint

Through the native Sniffmail API, this operation is `GET /jobs/:jobId/results` (base URL `https://api.sniffmail.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-results.md) for the provider-specific parameters and requirements.

