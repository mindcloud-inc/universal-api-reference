# AddEvent: Retrieve calendar



```
GET https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-calendar?connectionId=$CONNECTION_ID&calendarId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-calendar?${params}`, {
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
| `calendarId` | string | yes | Unique identifier for the calendar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarColor": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "embeddableCalendarTemplateId": "string",
      "eventDefaultTemplateId": "string",
      "id": "string",
      "internalName": "Ava Chen",
      "isDefaultCalendar": true,
      "landingPageTemplateId": "string",
      "linkLong": "https://example.com",
      "linkShort": "https://example.com",
      "modified": "2026-05-07T12:00:00.000Z",
      "paletteId": "string",
      "stats": {
        "eventsCount": 1,
        "subscribersActiveCount": 1,
        "subscribersAllCount": 1
      },
      "timezone": "string",
      "title": "string",
      "uniqueKey": "string",
      "weekdayBegin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarColor` | number | Calendar color value. |
| `created` | date | Calendar creation timestamp. |
| `description` | string | Calendar description. |
| `embeddableCalendarTemplateId` | string | Assigned embeddable calendar template ID. |
| `eventDefaultTemplateId` | string | Default event template ID. |
| `id` | string | Unique identifier for the calendar. |
| `internalName` | string | Internal-only calendar name. |
| `isDefaultCalendar` | boolean | Whether the calendar is the account default. |
| `landingPageTemplateId` | string | Assigned landing page template ID. |
| `linkLong` | string | Public long URL for the calendar. |
| `linkShort` | string | Public short URL for the calendar. |
| `modified` | date | Calendar last modified timestamp. |
| `paletteId` | string | Associated color palette ID. |
| `stats.eventsCount` | number |  |
| `stats.subscribersActiveCount` | number |  |
| `stats.subscribersAllCount` | number |  |
| `timezone` | string | Default timezone for calendar events. |
| `title` | string | Calendar title. |
| `uniqueKey` | string | Public identifier for the calendar. |
| `weekdayBegin` | string | Day that the calendar starts on. |

## Native endpoint

Through the native AddEvent API, this operation is `GET /calendars/:calendar_id` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-calendar.md) for the provider-specific parameters and requirements.

