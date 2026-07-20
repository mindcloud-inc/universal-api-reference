# AddEvent: Search events



```
GET https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-events?${params}`, {
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
| `calendarIds[]` | array<string> | no | Comma-separated list of calendar IDs. Limits search results to those specific calendars. Accepts multiple values in one string, delimited by `,`. |
| `eventIds[]` | array<string> | no | Comma-separated list of event IDs. Limits search results to those specific events. Accepts multiple values in one string, delimited by `,`. |
| `datetimeMin` | string | no | Limits search results to events that end after this time. |
| `datetimeMax` | string | no | Limits search results to events that start before this time. |
| `search` | string | no | Search term applied across event title, internal name, description, and location. |
| `customDataKey` | string | no | Custom data key to pair with Custom Data Value when filtering results. |
| `customDataValue` | string | no | Custom data value to pair with Custom Data Key when filtering results. |

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

Through the native AddEvent API, this operation is `GET /events` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-events.md) for the provider-specific parameters and requirements.

