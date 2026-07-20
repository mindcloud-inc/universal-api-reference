# Clappia: Update Workflow Step

Updates an existing workflow step in Clappia.

```
PUT https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-workflow-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-workflow-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "triggerType": "string",
  "stepVariableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-workflow-step', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "triggerType": "string",
    "stepVariableName": "Ava Chen"
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
| `stepVariableName` | string | yes | Variable name of the existing workflow step to update. |
| `name` | string | no | Updated display name for the workflow step. |
| `instructions` | string | no | Updated node instructions, such as AI prompt text. |
| `model` | string | no | Updated model identifier for supported AI nodes. |
| `llm` | string | no | Updated LLM provider for supported AI nodes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stepName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stepName` | string |  |

## Native endpoint

Through the native Clappia API, this operation is `POST /workflowdefinitionv2/updateWorkflowStep` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow-step.md) for the provider-specific parameters and requirements.

