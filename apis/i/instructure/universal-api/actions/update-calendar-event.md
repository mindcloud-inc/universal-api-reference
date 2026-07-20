# Instructure: Update Calendar Event

Updates an existing calendar event in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-calendar-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-calendar-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-calendar-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | The Canvas calendar event ID. Default: `1`. |
| `startAt` | string | no | The calendar event start datetime in ISO-8601 format. Default: `2026-04-10T15:00:00Z`. |
| `title` | string | no | The updated calendar event title. Default: `MindCloud Validation Event`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDay": true,
      "contextCode": "string",
      "description": "string",
      "endAt": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "locationName": "Ava Chen",
      "startAt": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | boolean |  |
| `contextCode` | string |  |
| `description` | string |  |
| `endAt` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `locationName` | string |  |
| `startAt` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `PUT /calendar_events/:event_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-calendar-event.md) for the provider-specific parameters and requirements.

