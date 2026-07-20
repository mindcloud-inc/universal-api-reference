# Worksnaps: Create a task assignment (i.e., assign a user to a task)

Creates a task assignment in a Worksnaps project.

```
POST https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-task-assignment-ie-assign-a-user-to-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-task-assignment-ie-assign-a-user-to-a-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-task-assignment-ie-assign-a-user-to-a-task', {
  method: 'POST',
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
| `body` | string | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | string | no | ID of the target project that the task is in |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "project_id": 1,
      "task_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | the ID of the task assignment |
| `project_id` | number | the ID of the project |
| `task_id` | number | the Id of the task |
| `user_id` | number | the ID of the user |

## Native endpoint

Through the native Worksnaps API, this operation is `POST /projects/{project_id}/task_assignments.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-task-assignment-ie-assign-a-user-to-a-task.md) for the provider-specific parameters and requirements.

