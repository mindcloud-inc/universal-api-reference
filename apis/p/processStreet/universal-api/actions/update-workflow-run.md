# Process Street: Update Workflow Run



```
PUT https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/update-workflow-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/update-workflow-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowRunId": "string",
  "name": "Ava Chen",
  "status": "string",
  "shared": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/update-workflow-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowRunId": "string",
    "name": "Ava Chen",
    "status": "string",
    "shared": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowRunId` | string | yes | The ID of the workflow run. |
| `name` | string | yes | The workflow run name. |
| `status` | string | yes | The workflow run status. |
| `shared` | boolean | yes | Whether the workflow run is shared. |
| `dueDate` | date | no | Optional due date for the workflow run. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Street API returns.

## Native endpoint

Through the native Process Street API, this operation is `PUT /workflow-runs/:workflowRunId` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow-run.md) for the provider-specific parameters and requirements.

