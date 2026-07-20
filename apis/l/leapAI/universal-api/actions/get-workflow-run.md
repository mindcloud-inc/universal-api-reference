# Leap AI: Get Workflow Run

Retrieves a workflow run from Leap AI.

```
GET https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/get-workflow-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leap AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/get-workflow-run?connectionId=$CONNECTION_ID&workflowRunId=runv2_8R8jNYkpBVLI4FqCJiJ5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowRunId": "runv2_8R8jNYkpBVLI4FqCJiJ5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/get-workflow-run?${params}`, {
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
| `workflowRunId` | string | yes | The runv2_ identifier of the workflow run to retrieve. Example: `runv2_8R8jNYkpBVLI4FqCJiJ5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "error": "string",
      "id": "string",
      "result": {},
      "status": "string",
      "version_id": "string",
      "workflow_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Workflow run creation timestamp. |
| `error` | string | Error message when the run fails or null otherwise. |
| `id` | string | Workflow run identifier. |
| `result` | object | Workflow result payload object or null. |
| `status` | string | Current workflow run status. |
| `version_id` | string | Workflow version identifier. |
| `workflow_id` | string | Published workflow identifier. |

## Native endpoint

Through the native Leap AI API, this operation is `GET /v2/runs/:workflowRunId` (base URL `https://api.workflows.tryleap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-run.md) for the provider-specific parameters and requirements.

