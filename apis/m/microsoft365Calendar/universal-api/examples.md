# Microsoft 365 Calendar Universal API Examples

These examples use the MindCloud API key and Microsoft 365 Calendar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Calendars

Retrieves calendars from Microsoft 365 Calendar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendars?${params}`, {
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
      "canEdit": true,
      "canShare": true,
      "color": "string",
      "id": "string",
      "isDefaultCalendar": true,
      "isRemovable": true,
      "name": "Ava Chen",
      "owner": {
        "address": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Calendars action reference](actions/list-calendars.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365Calendar/latest/actions/list-calendars).

## Accept Event

Accepts an event invitation in Microsoft 365 Calendar.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/accept-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/accept-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "AAMkAG..."
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

See the full [Accept Event action reference](actions/accept-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365Calendar/latest/actions/accept-event).
