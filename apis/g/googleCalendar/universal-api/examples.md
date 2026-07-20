# Google Calendar Universal API Examples

These examples use the MindCloud API key and Google Calendar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Calendars

Retrieves calendar list entries from Google Calendar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-calendars?${params}`, {
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
      "accessRole": "string",
      "backgroundColor": "string",
      "colorId": "string",
      "conferenceProperties": {
        "allowedConferenceSolutionTypes": [
          "string"
        ]
      },
      "defaultReminders": [
        {
          "method": "string",
          "minutes": 1
        }
      ],
      "etag": "string",
      "foregroundColor": "string",
      "id": "string",
      "kind": "string",
      "notificationSettings": {
        "notifications": [
          {
            "method": "string",
            "type": "string"
          }
        ]
      },
      "primary": true,
      "selected": true,
      "summary": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Calendars action reference](actions/list-calendars.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleCalendar/latest/actions/list-calendars).

## Add Calendar to List

Adds an existing calendar to the Google Calendar list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/add-calendar-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/add-calendar-to-list', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add Calendar to List action reference](actions/add-calendar-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleCalendar/latest/actions/add-calendar-to-list).
