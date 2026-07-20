# Calendly: List Event Type Available Times

Retrieves available times for a Calendly event type.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-event-type-available-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-event-type-available-times?connectionId=$CONNECTION_ID&event_type=https%3A%2F%2Fapi.calendly.com%2Fevent_types%2F8d38b11a-269e-4878-ab4a-12048b63906d&start_time=2026-03-01T15%3A00%3A00Z&end_time=2026-03-01T16%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event_type": "https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d",
  "start_time": "2026-03-01T15:00:00Z",
  "end_time": "2026-03-01T16:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-event-type-available-times?${params}`, {
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
| `event_type` | list | yes | Event type URI. One of: `https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d`. Default: `https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d`. |
| `start_time` | date | yes | Start of interval (ISO-8601). Default: `2026-03-01T15:00:00Z`. |
| `end_time` | date | yes | End of interval (ISO-8601). Default: `2026-03-01T16:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> | Available time slot records for the event type. |

## Native endpoint

Through the native Calendly API, this operation is `GET /event_type_available_times` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-type-available-times.md) for the provider-specific parameters and requirements.

