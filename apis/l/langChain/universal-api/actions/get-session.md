# LangChain: Get Session



```
GET https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-session?${params}`, {
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
| `sessionId` | string | yes | Session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completion_cost": 1,
      "completion_tokens": 1,
      "default_dataset_id": "string",
      "description": "string",
      "end_time": "2026-05-07T12:00:00.000Z",
      "error_rate": 1,
      "extra": {},
      "feedback_stats": {},
      "first_token_p50": 1,
      "first_token_p99": 1,
      "id": "string",
      "last_run_start_time": "2026-05-07T12:00:00.000Z",
      "last_run_start_time_live": "2026-05-07T12:00:00.000Z",
      "latency_p50": 1,
      "latency_p99": 1,
      "name": "Ava Chen",
      "prompt_cost": 1,
      "prompt_tokens": 1,
      "reference_dataset_id": "string",
      "run_count": 1,
      "run_facets": {},
      "session_feedback_stats": {},
      "start_time": "2026-05-07T12:00:00.000Z",
      "streaming_rate": 1,
      "tenant_id": "string",
      "test_run_number": 1,
      "total_cost": 1,
      "total_tokens": 1,
      "trace_tier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completion_cost` | number | Completion cost. |
| `completion_tokens` | number | Completion tokens. |
| `default_dataset_id` | string | Optional default dataset UUID. |
| `description` | string | Session description. |
| `end_time` | date | Session end timestamp. |
| `error_rate` | number | Error rate. |
| `extra` | object | Additional metadata. |
| `feedback_stats` | object | Feedback aggregates. |
| `first_token_p50` | number | P50 first-token latency. |
| `first_token_p99` | number | P99 first-token latency. |
| `id` | string | Session UUID. |
| `last_run_start_time` | date | Last run start timestamp. |
| `last_run_start_time_live` | date | Last live run start timestamp. |
| `latency_p50` | number | P50 latency. |
| `latency_p99` | number | P99 latency. |
| `name` | string | Session name. |
| `prompt_cost` | number | Prompt cost. |
| `prompt_tokens` | number | Prompt tokens. |
| `reference_dataset_id` | string | Optional reference dataset UUID. |
| `run_count` | number | Run count. |
| `run_facets` | object | Run facets. |
| `session_feedback_stats` | object | Session feedback aggregates. |
| `start_time` | date | Session start timestamp. |
| `streaming_rate` | number | Streaming rate. |
| `tenant_id` | string | Workspace UUID. |
| `test_run_number` | number | Test run number. |
| `total_cost` | number | Total cost. |
| `total_tokens` | number | Total tokens. |
| `trace_tier` | string | Trace retention tier. |

## Native endpoint

Through the native LangChain API, this operation is `GET /api/v1/sessions/:sessionId` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

