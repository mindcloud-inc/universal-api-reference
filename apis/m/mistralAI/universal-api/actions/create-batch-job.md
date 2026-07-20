# Mistral AI: Create Batch Job

Creates a new batch job in Mistral AI.

```
POST https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/create-batch-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/create-batch-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpoint": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/create-batch-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpoint": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpoint` | string | yes | Endpoint path that the batch job should execute. |
| `inputFiles[]` | array<string> | no | Uploaded JSONL input files for the batch job. |
| `requests[]` | array<object> | no | Inline batch request objects. |
| `model` | string | no | Optional model override for the batch job. |
| `agentId` | string | no | Optional deprecated agent ID for the batch job. |
| `metadata` | object | no | Metadata to associate with the batch job. |
| `timeoutHours` | number | no | Timeout in hours for the batch job. |

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

Through the native Mistral AI API, this operation is `POST /v1/batch/jobs` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-job.md) for the provider-specific parameters and requirements.

