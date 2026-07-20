# SignalWire: List Log Events

Retrieves voice log events from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-log-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-log-events?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-log-events?${params}`, {
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
| `id` | string | yes | Unique ID of the log. This is the segment_id you can find in Relay call details in your Dashboard UI or in return objects when using the SDK. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "event_at": "2026-05-07T12:00:00.000Z",
      "level": "string",
      "log_id": "string",
      "name": "Ava Chen",
      "project_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Additional details about the event. Structure varies by event type. |
| `event_at` | date | Timestamp when the event occurred. |
| `level` | string | Log level of the event. |
| `log_id` | string | Unique identifier for the log. |
| `name` | string | Name of the event. |
| `project_id` | string | Unique identifier for the project. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /voice/logs/{id}/events` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-log-events.md) for the provider-specific parameters and requirements.

