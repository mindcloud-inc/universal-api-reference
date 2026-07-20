# Google Calendar: Create Event

Creates a new event in Google Calendar.

```
POST https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendar": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendar": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attendees[].email` | string | no |  |
| `calendar` | list | yes |  |
| `title` | string | no |  |
| `location` | string | no |  |
| `description` | string | no |  |
| `start` | date | no |  |
| `end` | date | no |  |
| `attendees[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {
          "email": "ava@example.com",
          "organizer": true,
          "responseStatus": "string",
          "self": true
        }
      ],
      "created": "string",
      "creator": {
        "email": "ava@example.com",
        "self": true
      },
      "description": "string",
      "end": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "etag": "string",
      "eventType": "string",
      "htmlLink": "https://example.com",
      "iCalUID": "string",
      "id": "string",
      "kind": "string",
      "organizer": {
        "email": "ava@example.com",
        "self": true
      },
      "reminders": {
        "useDefault": true
      },
      "sequence": 1,
      "start": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "status": "string",
      "summary": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees[].email` | string |  |
| `attendees[].organizer` | boolean |  |
| `attendees[].responseStatus` | string |  |
| `attendees[].self` | boolean |  |
| `created` | string |  |
| `creator.email` | string |  |
| `creator.self` | boolean |  |
| `description` | string |  |
| `end.dateTime` | string |  |
| `end.timeZone` | string |  |
| `etag` | string |  |
| `eventType` | string |  |
| `htmlLink` | string |  |
| `iCalUID` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `organizer.email` | string |  |
| `organizer.self` | boolean |  |
| `reminders.useDefault` | boolean |  |
| `sequence` | number |  |
| `start.dateTime` | string |  |
| `start.timeZone` | string |  |
| `status` | string |  |
| `summary` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Google Calendar API, this operation is `POST calendars/:calendar/events` (base URL `https://www.googleapis.com/calendar/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

