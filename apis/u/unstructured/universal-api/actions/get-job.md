# Unstructured: Get Job

Retrieves a job from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-job?${params}`, {
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
| `jobId` | string | yes | The job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "inputFileIds": [
        [
          "string"
        ]
      ],
      "jobType": "string",
      "outputNodeFiles": [
        [
          {}
        ]
      ],
      "runtime": "string",
      "status": "string",
      "workflowId": "string",
      "workflowName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `id` | string | Job ID. |
| `inputFileIds[]` | array<string> | Input file IDs. |
| `jobType` | string | Job type. |
| `outputNodeFiles[]` | array<object> | Output node files. |
| `runtime` | string | Job runtime duration. |
| `status` | string | Job status. |
| `workflowId` | string | Workflow ID. |
| `workflowName` | string | Workflow name. |

## Native endpoint

Through the native Unstructured API, this operation is `GET /jobs/:job_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

