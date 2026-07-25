# Worksnaps: Delete a Task Assignment by ID

Deletes an existing task assignment from Worksnaps.

```
DELETE https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/delete-a-task-assignment-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/delete-a-task-assignment-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/delete-a-task-assignment-by-id?${params}`, {
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
| `task_assignment_id` | string | no | ID of the task assignment to be deleted |

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

Through the native Worksnaps API, this operation is `DELETE /projects/{project_id}/task_assignments/{task_assignment_id}.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-task-assignment-by-id.md) for the provider-specific parameters and requirements.

