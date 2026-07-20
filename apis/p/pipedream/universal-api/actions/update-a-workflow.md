# Pipedream: Update a workflow

Updates an existing workflow in Pipedream.

```
PUT https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/update-a-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/update-a-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "workflowId": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/update-a-workflow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": true,
    "workflowId": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | yes | Set to true to activate the workflow or false to deactivate it. |
| `workflowId` | string | yes | The workflow identifier. |
| `workspaceId` | string | yes | The workspace organization ID that owns the workflow. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedream API returns.

## Native endpoint

Through the native Pipedream API, this operation is `PUT /workflows/{id}` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-workflow.md) for the provider-specific parameters and requirements.

