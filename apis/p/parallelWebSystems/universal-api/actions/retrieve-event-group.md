# Parallel Web Systems: Retrieve Event Group



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-event-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-event-group?connectionId=$CONNECTION_ID&eventGroupId=string&monitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventGroupId": "string",
  "monitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-event-group?${params}`, {
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
| `eventGroupId` | string | yes | The Parallel event group ID. |
| `monitorId` | string | yes | The Parallel monitor ID. |

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

Through the native Parallel Web Systems API, this operation is `GET /v1alpha/monitors/:monitor_id/event_groups/:event_group_id` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-event-group.md) for the provider-specific parameters and requirements.

