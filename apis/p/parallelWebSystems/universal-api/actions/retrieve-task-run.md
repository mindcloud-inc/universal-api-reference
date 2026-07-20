# Parallel Web Systems: Retrieve Task Run



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-task-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-task-run?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-task-run?${params}`, {
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
| `runId` | string | yes | The Parallel task run ID. |

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

Through the native Parallel Web Systems API, this operation is `GET /v1/tasks/runs/:run_id` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task-run.md) for the provider-specific parameters and requirements.

