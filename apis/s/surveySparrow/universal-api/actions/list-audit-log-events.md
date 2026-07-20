# SurveySparrow: List Audit Log Events

Retrieves subscribed audit log events from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-audit-log-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-audit-log-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-audit-log-events?${params}`, {
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
| `eventType` | list | no | Type of the event |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "events": [
        {}
      ],
      "has_next_page": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `events` | array<object> |  |
| `has_next_page` | boolean |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /audit_logs/events` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audit-log-events.md) for the provider-specific parameters and requirements.

