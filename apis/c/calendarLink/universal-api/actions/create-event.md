# CalendarLink: Create Event

Creates a new event in a CalendarLink organization.

```
POST https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "organization": "string",
  "title": "string",
  "start": "string",
  "end": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "organization": "string",
    "title": "string",
    "start": "string",
    "end": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | list<string> | yes | Collection ID that owns the event. |
| `organization` | string | yes | CalendarLink organization ID. |
| `rsvp.enabled` | boolean | no | Whether RSVP is enabled for the event. |
| `rsvp.settings.maxAttendees` | number | no | Maximum RSVP attendee count. |
| `rsvp.description` | string | no | RSVP description shown to invitees. |
| `rsvp.settings.notification` | string | no | RSVP notification mode. |
| `title` | string | yes | Event title. |
| `rsvp.deadline` | string | no | RSVP deadline timestamp. |
| `rsvp.settings.notificationEmail` | string | no | Email used for RSVP notifications. |
| `start` | string | yes | Event start datetime in `YYYY-MM-DD HH:MM:SS` format. |
| `end` | string | yes | Event end datetime in `YYYY-MM-DD HH:MM:SS` format. |
| `rsvp.settings.phoneEnabled` | boolean | no | Whether phone input is enabled for RSVP. |
| `rsvp.settings.descriptionEnabled` | boolean | no | Whether the RSVP description field is enabled. |
| `timezone` | string | no | Timezone identifier for the event. |
| `dateFormat` | string | no | Date format preference. |
| `rsvp.settings.descriptionLabel` | string | no | Label shown for the RSVP description field. |
| `description` | string | no | Event description. |
| `location` | string | no | Event location text. |
| `locationUrl` | string | no | Event location URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isRecurring": true,
      "location": "string",
      "locationUrl": "https://example.com",
      "rsvp": {},
      "start": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "timezone": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `end` | date |  |
| `id` | string |  |
| `isRecurring` | boolean |  |
| `location` | string |  |
| `locationUrl` | string |  |
| `rsvp` | object |  |
| `start` | date |  |
| `state` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native CalendarLink API, this operation is `POST /:organisation/event` (base URL `https://my.calendarlink.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

