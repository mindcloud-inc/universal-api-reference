# PromptLayer Run Agent: Run Agent

Runs a PromptLayer workflow.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/run-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/run-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowName": "wizard-stage3-agent-20260424-b"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/run-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowName": "wizard-stage3-agent-20260424-b"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowName` | string | yes | Name of the PromptLayer agent to run. Example: `wizard-stage3-agent-20260424-b`. |
| `workflowLabelName` | string | no | Optional release label for the agent version to run. Example: `production`. |
| `workflowVersionNumber` | number | no | Optional agent version number to run. Example: `1`. |
| `metadata` | object | no | Optional metadata attached to this execution. Example: `[object Object]`. |
| `inputVariables` | object | no | Optional input variables for the agent execution. Example: `[object Object]`. |
| `returnAllOutputs` | boolean | no | Whether to return all output nodes instead of only the final output. Example: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional webhook URL for asynchronous completion delivery. Example: `https://example.com/webhooks/promptlayer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "warning": "string",
      "workflowVersionExecutionId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |
| `warning` | string |  |
| `workflowVersionExecutionId` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /workflows/:workflow_name/run` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-agent.md) for the provider-specific parameters and requirements.

