# PagePixels: Get Website Domain Research Job Status



```
GET https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-website-domain-research-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-website-domain-research-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-website-domain-research-job-status?${params}`, {
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
| `jobId` | string | yes | The PagePixels domain research job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDomains": 1,
      "failedDomains": 1,
      "jobId": "string",
      "name": "Ava Chen",
      "percentComplete": 1,
      "status": "string",
      "totalDomains": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedDomains` | number | The number of domains processed successfully so far. |
| `failedDomains` | number | The number of domains that failed processing. |
| `jobId` | string | The unique identifier for the domain research job. |
| `name` | string | The name of the domain research job. |
| `percentComplete` | number | The completion percentage reported by PagePixels. |
| `status` | string | The current provider status for the job. |
| `totalDomains` | number | The total number of domains included in the job. |

## Native endpoint

Through the native PagePixels API, this operation is `GET /api/domain_research_requests/:job_id/status` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website-domain-research-job-status.md) for the provider-specific parameters and requirements.

