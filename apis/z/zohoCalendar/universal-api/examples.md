# Zoho Calendar Universal API Examples

These examples use the MindCloud API key and Zoho Calendar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Calendars

Retrieves user calendars from Zoho Calendar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-calendars?${params}`, {
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
      "calendars": [
        {
          "alarm": [
            {
              "action": "string",
              "trigger": "string"
            }
          ],
          "calendar_createdtime": 1,
          "calendar_modifiedtime": 1,
          "caltype": "string",
          "canSendMail": true,
          "category": "string",
          "color": "string",
          "createdtime": 1,
          "ctag": 1,
          "description": "string",
          "id": "string",
          "include_infreebusy": true,
          "isdefault": true,
          "lastmodifiedtime": "2026-05-07T12:00:00.000Z",
          "modifiedtime": 1,
          "name": "Ava Chen",
          "order": 1,
          "owner": "string",
          "privilege": "string",
          "reminders": [
            {
              "action": "string",
              "minutes": "string"
            }
          ],
          "status": true,
          "textcolor": "string",
          "timezone": "string",
          "type": 1,
          "uid": "string",
          "visibility": true
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Calendars action reference](actions/list-calendars.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCalendar/latest/actions/list-calendars).

## Create Calendar

Creates a new personal calendar in Zoho Calendar.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-calendar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarData": {}
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
      "calendars": [
        {
          "caltype": "string",
          "category": "string",
          "color": "string",
          "description": "string",
          "id": "string",
          "include_infreebusy": true,
          "name": "Ava Chen",
          "status": true,
          "textcolor": "string",
          "timezone": "string",
          "uid": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Calendar action reference](actions/create-calendar.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCalendar/latest/actions/create-calendar).
