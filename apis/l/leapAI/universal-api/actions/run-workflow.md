# Leap AI: Run Workflow

Runs a published workflow in Leap AI.

```
POST https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/run-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leap AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/run-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "wkfv2_bZNg4zPR44mA"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/run-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "wkfv2_bZNg4zPR44mA"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | string | yes | The wkfv2_ identifier of the published workflow to run. Example: `wkfv2_bZNg4zPR44mA`. |
| `triggerId` | string | no | The trigger node ID used to start the workflow. Example: `ncc6725`. |
| `webhookUrl` | string | no | Optional URL that Leap calls when the workflow run finishes. Example: `https://example.com/webhook`. |
| `input` | object | no | Optional object of workflow input variables. Example: `[object Object]`. |

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

Through the native Leap AI API, this operation is `POST /v2/runs` (base URL `https://api.workflows.tryleap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-workflow.md) for the provider-specific parameters and requirements.

