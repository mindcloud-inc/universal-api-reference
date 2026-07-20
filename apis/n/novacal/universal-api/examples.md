# Novacal Universal API Examples

These examples use the MindCloud API key and Novacal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Availability

Retrieves availability from Novacal.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-availability?${params}`, {
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
      "availability": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Availability action reference](actions/get-availability.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/novacal/latest/actions/get-availability).

## Book Event

Creates a new event booking in Novacal.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/book-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novacal/latest/actions/book-event', {
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
      "end": "2026-05-07T12:00:00.000Z",
      "event_type_id": 1,
      "form_field_answers": {},
      "id": "string",
      "location": {},
      "name": "Ava Chen",
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Book Event action reference](actions/book-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/novacal/latest/actions/book-event).
