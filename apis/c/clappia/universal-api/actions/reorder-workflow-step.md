# Clappia: Reorder Workflow Step

Updates workflow step order in Clappia.

```
PUT https://connect.mindcloud.co/v1/universal/clappia/latest/actions/reorder-workflow-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/reorder-workflow-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "triggerType": "string",
  "stepVariableName": "Ava Chen",
  "parentVariableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/reorder-workflow-step', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "triggerType": "string",
    "stepVariableName": "Ava Chen",
    "parentVariableName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clappia app ID. |
| `triggerType` | string | yes | Workflow trigger type, such as newSubmission, editSubmission, or reviewSubmission. |
| `stepVariableName` | string | yes | Variable name of the workflow step being moved. |
| `parentVariableName` | string | yes | Variable name of the new parent workflow step. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /workflowdefinitionv2/reorderWorkflowStep` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reorder-workflow-step.md) for the provider-specific parameters and requirements.

