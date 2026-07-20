# Parallel Web Systems: Stream Task Group Events



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-task-group-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-task-group-events?connectionId=$CONNECTION_ID&taskgroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskgroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-task-group-events?${params}`, {
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
| `taskgroupId` | string | yes | The Parallel task group ID. |
| `lastEventId` | string | no | Resume streaming after this event ID. |
| `timeout` | number | no | Long-poll timeout in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_id": "string",
      "status": {
        "is_active": true,
        "modified_at": "2026-05-07T12:00:00.000Z",
        "num_task_runs": 1,
        "status_message": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_id` | string | Event identifier. |
| `status.is_active` | boolean | Whether the task group is active. |
| `status.modified_at` | date | Last task group status update timestamp. |
| `status.num_task_runs` | number | Number of runs in the task group. |
| `status.status_message` | string | Task group status message. |
| `type` | string | Event type. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `GET /v1beta/tasks/groups/:taskgroup_id/events` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-task-group-events.md) for the provider-specific parameters and requirements.

