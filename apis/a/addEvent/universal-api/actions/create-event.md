# AddEvent: Create event



```
POST https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/create-event', {
  method: 'POST',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | The event title. |
| `calendarId` | string | no | Calendar ID to associate with the event. |
| `datetimeStart` | string | no | Start date and time for the event. |
| `datetimeEnd` | string | no | End date and time for the event. |
| `allDayEvent` | boolean | no | Whether the event should be treated as an all-day event. Default: `false`. |
| `timezone` | string | no | Timezone for the event. |
| `recurringRule` | string | no | iCalendar RRULE value for recurring events. |
| `description` | string | no | Event description shown to attendees. |
| `internalName` | string | no | Internal-only event name. |
| `location` | string | no | Address or URL for the event location. |
| `locationId` | number | no | Saved location ID to associate with the event. |
| `organizerName` | string | no | Organizer name displayed on the event. |
| `organizerEmail` | string | no | Organizer email displayed on the event. |
| `reminder` | number | no | Minutes before start time to send a reminder. Default: `30`. |
| `color` | number | no | Palette color value for the event. Default: `1`. |
| `freeBusy` | string | no | Whether the event appears as free, busy, or uses the default. Default: `default`. |
| `landingPageTemplateId` | string | no | Custom event landing page template ID or default. Default: `default`. |
| `rsvpEnabled` | boolean | no | Whether attendees must RSVP before adding the event. Default: `false`. |
| `rsvpFormId` | string | no | Custom RSVP form ID or default. Default: `default`. |
| `customData` | object | no | Structured key-value data attached to the event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDayEvent": true,
      "calendarId": "string",
      "color": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "datetimeEnd": "2026-05-07T12:00:00.000Z",
      "datetimeStart": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "freeBusy": "string",
      "id": "string",
      "internalName": "Ava Chen",
      "landingPageTemplateId": "string",
      "linkLong": "https://example.com",
      "linkShort": "https://example.com",
      "location": "string",
      "locationId": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "organizerEmail": "ava@example.com",
      "organizerName": "Ava Chen",
      "recurringRule": "string",
      "reminder": 1,
      "rsvp": {
        "settings": {
          "inactive": true,
          "notifyEmails": "ava@example.com",
          "notifyFrequency": "string",
          "rsvpFormId": "string",
          "rsvpInactiveBefore": 1,
          "rsvpInactiveMessage": "string",
          "rsvpSeatsExceedMessage": "string",
          "seatsLimit": 1,
          "seatsLimited": true
        },
        "stats": {
          "countCantgo": 1,
          "countGoing": 1,
          "countMaybe": 1,
          "countTotal": 1,
          "seatsLeft": 1
        }
      },
      "rsvpEnabled": true,
      "timezone": "string",
      "title": "string",
      "uniqueKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDayEvent` | boolean | Whether the event is all-day. |
| `calendarId` | string | Associated calendar ID. |
| `color` | number | Event color value. |
| `created` | date | Event creation timestamp. |
| `datetimeEnd` | date | Event end timestamp. |
| `datetimeStart` | date | Event start timestamp. |
| `description` | string | Event description. |
| `freeBusy` | string | Free/busy visibility setting. |
| `id` | string | Unique identifier for the event. |
| `internalName` | string | Internal-only event name. |
| `landingPageTemplateId` | string | Assigned event landing page template ID. |
| `linkLong` | string | Public long URL for the event. |
| `linkShort` | string | Public short URL for the event. |
| `location` | string | Event location. |
| `locationId` | number | Saved location ID. |
| `modified` | date | Event last modified timestamp. |
| `organizerEmail` | string | Organizer email. |
| `organizerName` | string | Organizer name. |
| `recurringRule` | string | Recurring rule in iCalendar format. |
| `reminder` | number | Reminder lead time in minutes. |
| `rsvp.settings.inactive` | boolean |  |
| `rsvp.settings.notifyEmails` | string |  |
| `rsvp.settings.notifyFrequency` | string |  |
| `rsvp.settings.rsvpFormId` | string |  |
| `rsvp.settings.rsvpInactiveBefore` | number |  |
| `rsvp.settings.rsvpInactiveMessage` | string |  |
| `rsvp.settings.rsvpSeatsExceedMessage` | string |  |
| `rsvp.settings.seatsLimit` | number |  |
| `rsvp.settings.seatsLimited` | boolean |  |
| `rsvp.stats.countCantgo` | number |  |
| `rsvp.stats.countGoing` | number |  |
| `rsvp.stats.countMaybe` | number |  |
| `rsvp.stats.countTotal` | number |  |
| `rsvp.stats.seatsLeft` | number |  |
| `rsvpEnabled` | boolean | Whether the event requires RSVP. |
| `timezone` | string | Event timezone. |
| `title` | string | Event title. |
| `uniqueKey` | string | Public identifier for the event. |

## Native endpoint

Through the native AddEvent API, this operation is `POST /events` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

