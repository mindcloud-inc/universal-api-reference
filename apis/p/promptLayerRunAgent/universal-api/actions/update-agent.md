# PromptLayer Run Agent: Update Agent

Updates an existing workflow in PromptLayer.

```
PUT https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowIdOrName": "wizard-stage3-agent-20260424-b",
  "nodes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowIdOrName": "wizard-stage3-agent-20260424-b",
    "nodes": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowIdOrName` | string | yes | The PromptLayer agent ID or name to update. Example: `wizard-stage3-agent-20260424-b`. |
| `baseVersion` | number | no | Optional version number to base the patch on. Example: `1`. |
| `commitMessage` | string | no | A message describing the update. Example: `Update greeting output`. |
| `nodes` | object | yes | Partial node updates keyed by existing or new node name. Example: `[object Object]`. |
| `requiredInputVariables` | object | no | Optional required input variable contract for the updated agent version. |
| `releaseLabels[]` | array<string> | no | Optional release labels to attach to the new agent version. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `edges[]` | array<object> | no | Optional full edge list to store on the new agent version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseVersion": 1,
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
| `baseVersion` | number |  |
| `nodes` | array<object> |  |
| `releaseLabels` | array<string> |  |
| `requiredInputVariables` | object |  |
| `success` | boolean |  |
| `versionNumber` | number |  |
| `workflowId` | number |  |
| `workflowName` | string |  |
| `workflowVersionId` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `PATCH /rest/workflows/:workflow_id_or_name` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

