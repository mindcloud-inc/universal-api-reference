# Clappia: Add Workflow Step

Creates a new workflow step in Clappia.

```
POST https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-workflow-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-workflow-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "triggerType": "string",
  "nodeType": "string",
  "parentVariableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-workflow-step', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "triggerType": "string",
    "nodeType": "string",
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
| `nodeType` | string | yes | Workflow node type, such as email, wait, condition, sms, approval, restApi, or ai. |
| `parentVariableName` | string | yes | Parent workflow step variable name under which the new step should be attached. |
| `toEmailAddresses[]` | array<string> | no | Recipient email addresses for email nodes. |
| `ccEmailAddresses[]` | array<string> | no | CC email addresses for email nodes. |
| `bccEmailAddresses[]` | array<string> | no | BCC email addresses for email nodes. |
| `subject` | string | no | Message subject for email or notification nodes. |
| `body` | string | no | Message or template body for the workflow step. |
| `replyTo` | string | no | Reply-to email address for email nodes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `staticAttachments[]` | array<object> | no | Static attachment objects for supported workflow nodes. |
| `printTemplateIndices[]` | array<number> | no | Print template indices to attach for supported nodes. |
| `dynamicAttachments[]` | array<string> | no | Field names whose files should be attached dynamically. |

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

Through the native Clappia API, this operation is `POST /workflowdefinitionv2/addWorkflowStep` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-workflow-step.md) for the provider-specific parameters and requirements.

