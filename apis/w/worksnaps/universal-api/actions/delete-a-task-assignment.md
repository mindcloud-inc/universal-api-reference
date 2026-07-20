# Worksnaps: Delete a task assignment

Deletes an existing task assignment from Worksnaps.

```
DELETE https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/delete-a-task-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/delete-a-task-assignment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/delete-a-task-assignment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | no | ID of the target project |
| `task_id` | string | no | ID of the target task |
| `user_id` | string | no | ID of the target user that need to be unassigned the specified task |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | Operation status. |

## Native endpoint

Through the native Worksnaps API, this operation is `DELETE /projects/{project_id}/task_assignments.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-task-assignment.md) for the provider-specific parameters and requirements.

