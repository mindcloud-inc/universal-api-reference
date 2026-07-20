# LangChain: Get Run



```
GET https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-run?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-run?${params}`, {
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
| `runId` | string | yes | Run identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app_path": "string",
      "completion_cost": 1,
      "completion_tokens": 1,
      "dotted_order": "string",
      "end_time": "2026-05-07T12:00:00.000Z",
      "error": {},
      "events": {},
      "execution_order": 1,
      "feedback_stats": {},
      "id": "string",
      "inputs": {},
      "name": "Ava Chen",
      "outputs": {},
      "parent_run_id": "string",
      "prompt_cost": 1,
      "prompt_tokens": 1,
      "run_type": "string",
      "session_id": "string",
      "start_time": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tags": {},
      "total_cost": 1,
      "total_tokens": 1,
      "trace_first_received_at": "2026-05-07T12:00:00.000Z",
      "trace_id": "string",
      "trace_tier": "string",
      "trace_upgrade": true,
      "ttl_seconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_path` | string | Provider app path. |
| `completion_cost` | number | Completion cost. |
| `completion_tokens` | number | Completion token count. |
| `dotted_order` | string | Trace ordering token. |
| `end_time` | date | Run end time. |
| `error` | object | Error details when failed. |
| `events` | object | Run events. |
| `execution_order` | number | Execution order in trace. |
| `feedback_stats` | object | Aggregated feedback stats. |
| `id` | string | Run UUID. |
| `inputs` | object | Run input payload. |
| `name` | string | Run name. |
| `outputs` | object | Run output payload. |
| `parent_run_id` | string | Optional parent run UUID. |
| `prompt_cost` | number | Prompt cost. |
| `prompt_tokens` | number | Prompt token count. |
| `run_type` | string | Run type. |
| `session_id` | string | Session UUID. |
| `start_time` | date | Run start time. |
| `status` | string | Run status. |
| `tags` | object | Run tags. |
| `total_cost` | number | Total cost. |
| `total_tokens` | number | Total tokens used. |
| `trace_first_received_at` | date | First trace receive timestamp. |
| `trace_id` | string | Trace UUID. |
| `trace_tier` | string | Trace retention tier. |
| `trace_upgrade` | boolean | Whether trace tier was upgraded. |
| `ttl_seconds` | number | Trace TTL in seconds. |

## Native endpoint

Through the native LangChain API, this operation is `GET /api/v1/runs/:runId` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run.md) for the provider-specific parameters and requirements.

