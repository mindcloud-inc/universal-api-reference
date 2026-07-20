# Novacal: Reschedule Event

Updates an existing event in Novacal.

```
PUT https://connect.mindcloud.co/v1/universal/novacal/latest/actions/reschedule-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/reschedule-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novacal/latest/actions/reschedule-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "event_type_id": 1,
      "id": "string",
      "location": {},
      "name": "Ava Chen",
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date | Event end time. |
| `event_type_id` | number | Associated event type ID. |
| `id` | string | Event ID. |
| `location` | object | Event location details. |
| `name` | string | Event name. |
| `start` | date | Event start time. |
| `status` | string | Event status. |

## Native endpoint

Through the native Novacal API, this operation is `PUT /v1/events/:id` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reschedule-event.md) for the provider-specific parameters and requirements.

