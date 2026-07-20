# Parallel Web Systems: Create Task Run



```
POST https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-task-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-task-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-task-run', {
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
      "error": {
        "message": "string"
      },
      "interaction_id": "string",
      "is_active": true,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "processor": "string",
      "run_id": "string",
      "status": "string",
      "taskgroup_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Task run creation timestamp. |
| `error.message` | string | Run error message when present. |
| `interaction_id` | string | Associated interaction identifier. |
| `is_active` | boolean | Whether the run is still active. |
| `modified_at` | date | Last task run update timestamp. |
| `processor` | string | Processor used for the run. |
| `run_id` | string | Parallel task run identifier. |
| `status` | string | Task run status. |
| `taskgroup_id` | string | Parent task group identifier. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `POST /v1/tasks/runs` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-run.md) for the provider-specific parameters and requirements.

