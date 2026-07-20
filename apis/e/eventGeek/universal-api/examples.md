# EventGeek Universal API Examples

These examples use the MindCloud API key and EventGeek connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events

Retrieves event records from your EventGeek account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-events?${params}`, {
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
      "end_date": "string",
      "id": "string",
      "location": "string",
      "name": "Ava Chen",
      "start_date": "string",
      "status": "string",
      "team_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventGeek/latest/actions/list-events).

## Add Contact To Event

Adds a contact to an event in EventGeek.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/add-contact-to-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": "Q29udGFjdC0xOTA3MjA",
  "event_id": "RXZlbnQtNzg5NDE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/add-contact-to-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": "Q29udGFjdC0xOTA3MjA",
    "event_id": "RXZlbnQtNzg5NDE"
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
      "attendance_status": "string",
      "contact_id": "string",
      "event_id": "string",
      "id": "string",
      "registration_status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact To Event action reference](actions/add-contact-to-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventGeek/latest/actions/add-contact-to-event).
