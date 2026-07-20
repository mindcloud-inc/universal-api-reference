# AddEvent: Retrieve event



```
GET https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-event?${params}`, {
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
| `eventId` | string | yes | Unique identifier for the event. |

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

Through the native AddEvent API, this operation is `GET /events/:event_id` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-event.md) for the provider-specific parameters and requirements.

