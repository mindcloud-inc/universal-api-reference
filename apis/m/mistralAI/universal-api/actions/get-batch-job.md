# Mistral AI: Get Batch Job

Retrieves batch job details from Mistral AI.

```
GET https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/get-batch-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/get-batch-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/get-batch-job?${params}`, {
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
| `jobId` | string | yes | The ID of the batch job. |
| `inline` | boolean | no | Include inline result content in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_id": "string",
      "completed_at": 1,
      "completed_requests": 1,
      "created_at": 1,
      "endpoint": "string",
      "error_file": "string",
      "errors": [
        {}
      ],
      "failed_requests": 1,
      "id": "string",
      "input_files": [
        "string"
      ],
      "metadata": {},
      "model": "string",
      "object": "string",
      "output_file": "string",
      "outputs": [
        {}
      ],
      "started_at": 1,
      "status": "string",
      "succeeded_requests": 1,
      "total_requests": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_id` | string |  |
| `completed_at` | number |  |
| `completed_requests` | number |  |
| `created_at` | number |  |
| `endpoint` | string |  |
| `error_file` | string |  |
| `errors` | array<object> |  |
| `failed_requests` | number |  |
| `id` | string |  |
| `input_files` | array<string> |  |
| `metadata` | object |  |
| `model` | string |  |
| `object` | string |  |
| `output_file` | string |  |
| `outputs` | array<object> |  |
| `started_at` | number |  |
| `status` | string |  |
| `succeeded_requests` | number |  |
| `total_requests` | number |  |

## Native endpoint

Through the native Mistral AI API, this operation is `GET /v1/batch/jobs/:job_id` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-job.md) for the provider-specific parameters and requirements.

