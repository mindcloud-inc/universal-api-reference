# Parallel Web Systems: Add Runs to Task Group



```
PUT https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/add-runs-to-task-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/add-runs-to-task-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskgroupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/add-runs-to-task-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskgroupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskgroupId` | string | yes | The Parallel task group ID. |
| `refreshStatus` | boolean | no | Refresh the task group status after adding runs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_cursor": "string",
      "run_cursor": "string",
      "run_ids": "string",
      "status": {
        "is_active": true,
        "modified_at": "2026-05-07T12:00:00.000Z",
        "num_task_runs": 1,
        "status_message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_cursor` | string | Cursor for event pagination. |
| `run_cursor` | string | Cursor for run pagination. |
| `run_ids` | string | Run identifiers added to the task group. |
| `status.is_active` | boolean | Whether the task group is active. |
| `status.modified_at` | date | Last task group status update timestamp. |
| `status.num_task_runs` | number | Number of runs in the task group. |
| `status.status_message` | string | Task group status message. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `POST /v1beta/tasks/groups/:taskgroup_id/runs` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-runs-to-task-group.md) for the provider-specific parameters and requirements.

