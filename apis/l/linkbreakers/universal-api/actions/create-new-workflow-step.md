# Linkbreakers: Create a New Workflow Step

Creates a new workflow step in Linkbreakers.

```
POST https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-new-workflow-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-new-workflow-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "linkId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-new-workflow-step', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "linkId": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkId` | string | yes | The ID of the link to create the workflow step for. |
| `canvasPosition` | object | no | Canvas position for the workflow step node. |
| `eventAction` | string | no | The event action type for the workflow step. |
| `id` | string | no | Optional workflow step ID. |
| `payload` | object | no | Workflow step payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "workflowStep": {
        "canvasPosition": {},
        "childStepIds": [
          "string"
        ],
        "createdAt": "string",
        "eventAction": "string",
        "id": "string",
        "kind": "string",
        "linkId": "https://example.com",
        "nodeType": "string",
        "parentStepIds": [
          "string"
        ],
        "payload": {},
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workflowStep` | object | Created workflow step. |
| `workflowStep.canvasPosition` | object |  |
| `workflowStep.childStepIds` | array<string> |  |
| `workflowStep.createdAt` | string |  |
| `workflowStep.eventAction` | string |  |
| `workflowStep.id` | string |  |
| `workflowStep.kind` | string |  |
| `workflowStep.linkId` | string |  |
| `workflowStep.nodeType` | string |  |
| `workflowStep.parentStepIds` | array<string> |  |
| `workflowStep.payload` | object |  |
| `workflowStep.updatedAt` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `POST /v1/links/:linkId/workflow-steps` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-workflow-step.md) for the provider-specific parameters and requirements.

