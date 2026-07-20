# Pipedream: Create a workflow

Creates a new workflow in Pipedream.

```
POST https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "settings": {},
  "steps[]": [
    {}
  ],
  "templateId": "string",
  "triggers[]": [
    {}
  ],
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "settings": {},
    "steps[]": [{}],
    "templateId": "string",
    "triggers[]": [{}],
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The project ID where the new workflow will be created. |
| `settings` | object | yes | Workflow settings such as name and auto_deploy. |
| `steps[]` | array<object> | yes | Definitions of the workflow steps, including namespace and props. |
| `templateId` | string | yes | The workflow template ID to base the new workflow on. |
| `triggers[]` | array<object> | yes | Definitions of the workflow triggers and their props. |
| `workspaceId` | string | yes | The workspace organization ID where the workflow will be created. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedream API returns.

## Native endpoint

Through the native Pipedream API, this operation is `POST /workflows` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-workflow.md) for the provider-specific parameters and requirements.

