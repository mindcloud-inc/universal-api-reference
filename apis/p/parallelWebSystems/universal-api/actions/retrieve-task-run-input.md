# Parallel Web Systems: Retrieve Task Run Input



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-task-run-input
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-task-run-input?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-task-run-input?${params}`, {
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
      "input": "string",
      "previous_interaction_id": "string",
      "processor": "string",
      "source_policy": {
        "after_date": "2026-05-07T12:00:00.000Z",
        "exclude_domains": "string",
        "include_domains": "string"
      },
      "task_spec": {
        "output_schema": {
          "type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input` | string | Task input payload. |
| `previous_interaction_id` | string | Previous interaction identifier. |
| `processor` | string | Processor used for the task run. |
| `source_policy.after_date` | date | Earliest source date. |
| `source_policy.exclude_domains` | string | Excluded domains filter. |
| `source_policy.include_domains` | string | Included domains filter. |
| `task_spec.output_schema.type` | string | Output schema type. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `GET /v1/tasks/runs/:run_id/input` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task-run-input.md) for the provider-specific parameters and requirements.

