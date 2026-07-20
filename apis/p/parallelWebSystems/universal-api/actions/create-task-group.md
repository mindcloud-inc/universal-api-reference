# Parallel Web Systems: Create Task Group



```
POST https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-task-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-task-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-task-group', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "status": {
        "is_active": true,
        "modified_at": "2026-05-07T12:00:00.000Z",
        "num_task_runs": 1,
        "status_message": "string"
      },
      "taskgroup_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Task group creation timestamp. |
| `status.is_active` | boolean | Whether the task group is active. |
| `status.modified_at` | date | Last task group status update timestamp. |
| `status.num_task_runs` | number | Number of runs in the task group. |
| `status.status_message` | string | Task group status message. |
| `taskgroup_id` | string | Task group identifier. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `POST /v1beta/tasks/groups` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-group.md) for the provider-specific parameters and requirements.

