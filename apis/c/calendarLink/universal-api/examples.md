# CalendarLink Universal API Examples

These examples use the MindCloud API key and CalendarLink connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from CalendarLink.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "organizations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calendarLink/latest/actions/get-current-user).

## Create Event

Creates a new event in a CalendarLink organization.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "organization": "string",
  "title": "string",
  "start": "string",
  "end": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "organization": "string",
    "title": "string",
    "start": "string",
    "end": "string"
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
      "description": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isRecurring": true,
      "location": "string",
      "locationUrl": "https://example.com",
      "rsvp": {},
      "start": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "timezone": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Event action reference](actions/create-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calendarLink/latest/actions/create-event).
