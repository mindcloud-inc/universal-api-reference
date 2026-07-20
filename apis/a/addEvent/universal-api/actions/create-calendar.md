# AddEvent: Create calendar



```
POST https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/create-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/create-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/create-calendar', {
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
| `title` | string | no | The calendar title. |
| `timezone` | string | no | Default timezone for events created on this calendar. Default: `America/Los_Angeles`. |
| `weekdayBegin` | string | no | Day of the week that the calendar starts on. Default: `sunday`. |
| `description` | string | no | Calendar description shown on the landing page. |
| `internalName` | string | no | Internal-only calendar name. |
| `calendarColor` | number | no | Calendar color value from the account palette. Default: `1`. |
| `landingPageTemplateId` | string | no | Custom landing page template ID or default. Default: `default`. |
| `embeddableCalendarTemplateId` | string | no | Custom embeddable calendar template ID or default. Default: `default`. |
| `customData` | object | no | Structured key-value data attached to the calendar. |

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

Through the native AddEvent API, this operation is `POST /calendars` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar.md) for the provider-specific parameters and requirements.

