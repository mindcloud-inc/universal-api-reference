# Instructure: Create Calendar Event

Creates a new calendar event in Instructure Canvas.

```
POST https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-calendar-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-calendar-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contextCode": "course_1",
  "endAt": "2026-04-10T16:00:00Z",
  "startAt": "2026-04-10T15:00:00Z",
  "title": "MindCloud Validation Event"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-calendar-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contextCode": "course_1",
    "endAt": "2026-04-10T16:00:00Z",
    "startAt": "2026-04-10T15:00:00Z",
    "title": "MindCloud Validation Event"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contextCode` | string | yes | The Canvas context code such as course_123 or user_247427066. Default: `course_1`. |
| `endAt` | string | yes | The calendar event end datetime in ISO-8601 format. Default: `2026-04-10T16:00:00Z`. |
| `startAt` | string | yes | The calendar event start datetime in ISO-8601 format. Default: `2026-04-10T15:00:00Z`. |
| `title` | string | yes | The calendar event title. Default: `MindCloud Validation Event`. |

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

Through the native Instructure API, this operation is `POST /calendar_events` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar-event.md) for the provider-specific parameters and requirements.

