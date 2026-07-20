# Diabolocom: Get Job Status

Retrieves a task job status from Diabolocom.

```
GET https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diabolocom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=job_123&expires=string&signature=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "job_123",
  "expires": "string",
  "signature": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | The Diabolocom job ID returned when a text or audio task was submitted. Example: `job_123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expires` | string | yes | Temporary expiry value from the job_status_endpoint_url returned by a Diabolocom job creation response. |
| `signature` | string | yes | Temporary signature value from the job_status_endpoint_url returned by a Diabolocom job creation response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "correlation_id": "string",
        "id": "string",
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
| `data.correlation_id` | string |  |
| `data.id` | string |  |
| `data.status` | string |  |

## Native endpoint

Through the native Diabolocom API, this operation is `GET https://execute.diabolocom.ai/api/job/status/:jobId` (base URL `https://api.diabolocom.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

