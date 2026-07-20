# Parallel Web Systems: List Monitor Events



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitor-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitor-events?connectionId=$CONNECTION_ID&monitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "monitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitor-events?${params}`, {
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
| `monitorId` | string | yes | The Parallel monitor ID. |
| `lookbackPeriod` | string | no | Lookback period to fetch events from, such as 10d or 1w. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": {
        "date": "2026-05-07T12:00:00.000Z",
        "error": "string",
        "event_date": "2026-05-07T12:00:00.000Z",
        "event_group_id": "string",
        "id": "string",
        "output": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events.date` | date | Event timestamp. |
| `events.error` | string | Event error message when present. |
| `events.event_date` | date | Event date. |
| `events.event_group_id` | string | Event group identifier. |
| `events.id` | string | Event identifier. |
| `events.output` | string | Event output payload. |
| `events.type` | string | Event type. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `GET /v1alpha/monitors/:monitor_id/events` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitor-events.md) for the provider-specific parameters and requirements.

