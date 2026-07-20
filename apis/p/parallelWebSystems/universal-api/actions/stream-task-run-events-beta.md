# Parallel Web Systems: Stream Task Run Events Beta



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-task-run-events-beta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-task-run-events-beta?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-task-run-events-beta?${params}`, {
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
      "event_id": "string",
      "message": "string",
      "progress_meter": 1,
      "source_stats": {
        "num_sources_considered": 1,
        "num_sources_read": 1
      },
      "timestamp": "2026-05-07T12:00:00.000Z",
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
| `message` | string | Progress message. |
| `progress_meter` | number | Progress percentage or fractional progress. |
| `source_stats.num_sources_considered` | number | Number of sources considered. |
| `source_stats.num_sources_read` | number | Number of sources read. |
| `timestamp` | date | Event timestamp. |
| `type` | string | Event type. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `GET /v1beta/tasks/runs/:run_id/events` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-task-run-events-beta.md) for the provider-specific parameters and requirements.

