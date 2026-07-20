# PromptLayer Run Agent: Create Agent

Creates a new workflow in PromptLayer.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample-agent-name",
  "nodes[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample-agent-name",
    "nodes[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the new PromptLayer agent. Example: `sample-agent-name`. |
| `nodes[]` | array<object> | yes | Workflow nodes array for the new agent. Example: `[object Object]`. |
| `commitMessage` | string | no | Message describing this agent version. Example: `Initial version`. |
| `requiredInputVariables` | object | no | Optional input variable map keyed by variable name. Example: `[object Object]`. |
| `releaseLabels[]` | array<string> | no | Optional release labels to attach to the created version. Example: `staging`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `edges[]` | array<object> | no | Optional conditional edge definitions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nodes": [
        {}
      ],
      "releaseLabels": [
        "string"
      ],
      "requiredInputVariables": {},
      "success": true,
      "versionNumber": 1,
      "workflowId": 1,
      "workflowName": "Ava Chen",
      "workflowVersionId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nodes` | array<object> | Created node summaries for the agent version. |
| `releaseLabels` | array<string> | Release labels attached to the created version. |
| `requiredInputVariables` | object | Required input variables map for the created agent. |
| `success` | boolean | Whether the agent creation succeeded. |
| `versionNumber` | number | Created agent version number. |
| `workflowId` | number | Numeric PromptLayer agent ID. |
| `workflowName` | string | Created agent name. |
| `workflowVersionId` | number | Created agent version ID. |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /rest/workflows` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

