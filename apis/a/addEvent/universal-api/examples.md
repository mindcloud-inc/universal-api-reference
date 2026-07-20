# AddEvent Universal API Examples

These examples use the MindCloud API key and AddEvent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search calendars



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-calendars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-calendars?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Search calendars action reference](actions/search-calendars.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/addEvent/latest/actions/search-calendars).

## Create calendar



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

Example response:

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

See the full [Create calendar action reference](actions/create-calendar.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/addEvent/latest/actions/create-calendar).
