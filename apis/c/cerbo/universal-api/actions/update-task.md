# Cerbo: Update Task

Updates an existing task in Cerbo.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task_id` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dr_id` | number | no | A valid ID of a non-archived, non-resource user who the task is being added for. |
| `subject` | string | no |  |
| `priority` | string | no |  |
| `notes` | string | no |  |
| `pt_id` | number | no | A valid ID of a non-archived patient to associate with the task. |
| `due_date` | date | no | A time stamp (YYYY-MM-DD HH:MM:SS format) representing the due date for this task. |
| `remind_minutes_before` | number | no | Represents the number of minutes before your due date to remind the user of the task (due_date must be set). |
| `completed_on` | date | no | Marks the task as complete or incomplete. Pass a valid timestamp (YYYY-MM-DD HH:MM:SS format) to mark complete. The date must be today or in the past — future dates are rejected. Pass null or false to reset the task to incomplete. |
| `associated_resource_type` | string | no | Links the task to a resource type (encounter note or document). Pass null or empty to unlink. If set, associated_resource_id must also be provided. If a pt_id is set, the linked resource must belong to the same patient. |
| `associated_resource_id` | number | no | The ID of the linked resource. Required when associated_resource_type is set. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `PATCH /task/:task_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

