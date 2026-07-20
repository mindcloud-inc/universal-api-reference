# Process Street: Approve or Reject Task



```
PUT https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/approve-or-reject-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/approve-or-reject-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowRunId": "string",
  "approvalTaskId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/approve-or-reject-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowRunId": "string",
    "approvalTaskId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowRunId` | string | yes | The ID of the workflow run. |
| `approvalTaskId` | string | yes | The ID of the approval task. |
| `subjectTaskId` | string | no | Optional subject task ID to approve or reject. |
| `status` | string | yes | Whether to approve or reject the task. |
| `comment` | string | no | Optional comment for the approval decision. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Street API returns.

## Native endpoint

Through the native Process Street API, this operation is `PUT /workflow-runs/:workflowRunId/approvals` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-or-reject-task.md) for the provider-specific parameters and requirements.

