# Datadog: List Events

Retrieves events from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-events?connectionId=$CONNECTION_ID&start=1&end=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "1",
  "end": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-events?${params}`, {
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
| `start` | number | yes | POSIX start timestamp. |
| `end` | number | yes | POSIX end timestamp. |
| `priority` | string | no | Event priority to filter by. |
| `sources` | string | no | Comma-separated event sources. |
| `tags` | string | no | Comma-separated tags for filtering events. |
| `unaggregated` | boolean | no | Return all events within the timeframe. |
| `excludeAggregate` | boolean | no | Return only unaggregated events. |
| `page` | number | no | Page number when using unaggregated event pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
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
| `events` | array<object> | Events returned by the request. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/events` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

