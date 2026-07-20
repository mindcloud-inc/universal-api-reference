# LangChain: Get Run Stats



```
GET https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-run-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-run-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-run-stats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "completion_cost": 1,
      "completion_cost_details": {},
      "completion_token_details": {},
      "completion_tokens": 1,
      "error_rate": 1,
      "feedback_stats": {},
      "first_token_p50": 1,
      "first_token_p99": 1,
      "last_run_start_time": "2026-05-07T12:00:00.000Z",
      "latency_p50": 1,
      "latency_p99": 1,
      "prompt_cost": 1,
      "prompt_cost_details": {},
      "prompt_token_details": {},
      "prompt_tokens": 1,
      "run_count": 1,
      "run_facets": {},
      "streaming_rate": 1,
      "total_cost": 1,
      "total_tokens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completion_cost` | number | Completion cost. |
| `completion_cost_details` | object | Completion cost details. |
| `completion_token_details` | object | Completion token details. |
| `completion_tokens` | number | Total completion tokens. |
| `error_rate` | number | Run error rate. |
| `feedback_stats` | object | Feedback aggregates. |
| `first_token_p50` | number | P50 first-token latency. |
| `first_token_p99` | number | P99 first-token latency. |
| `last_run_start_time` | date | Most recent run start timestamp. |
| `latency_p50` | number | P50 latency. |
| `latency_p99` | number | P99 latency. |
| `prompt_cost` | number | Prompt cost. |
| `prompt_cost_details` | object | Prompt cost details. |
| `prompt_token_details` | object | Prompt token details. |
| `prompt_tokens` | number | Total prompt tokens. |
| `run_count` | number | Number of runs in scope. |
| `run_facets` | object | Run facets. |
| `streaming_rate` | number | Streaming run rate. |
| `total_cost` | number | Total cost. |
| `total_tokens` | number | Total tokens. |

## Native endpoint

Through the native LangChain API, this operation is `POST /api/v1/runs/stats` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run-stats.md) for the provider-specific parameters and requirements.

