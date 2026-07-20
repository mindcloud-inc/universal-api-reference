# Dify: Get Workflow Run Detail

Retrieves workflow run details from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-workflow-run-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-workflow-run-detail?connectionId=$CONNECTION_ID&workflowRunId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowRunId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-workflow-run-detail?${params}`, {
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
| `workflowRunId` | string | yes | Workflow run ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "elapsedTime": 1,
      "error": "string",
      "finishedAt": 1,
      "id": "string",
      "inputs": {},
      "outputs": {},
      "status": "string",
      "totalSteps": 1,
      "totalTokens": 1,
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `elapsedTime` | number |  |
| `error` | string |  |
| `finishedAt` | number |  |
| `id` | string |  |
| `inputs` | object |  |
| `outputs` | object |  |
| `status` | string |  |
| `totalSteps` | number |  |
| `totalTokens` | number |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Dify API, this operation is `GET /workflows/run/:workflow_run_id` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-run-detail.md) for the provider-specific parameters and requirements.

