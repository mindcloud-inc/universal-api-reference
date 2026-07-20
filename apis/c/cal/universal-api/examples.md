# Cal.com Universal API Examples

These examples use the MindCloud API key and Cal.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bookings

Retrieves bookings from Cal.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-bookings?${params}`, {
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
      "attendees": [
        {}
      ],
      "createdAt": "string",
      "description": "string",
      "duration": 1,
      "end": "string",
      "eventTypeId": 1,
      "guests": [
        "string"
      ],
      "id": 1,
      "location": "string",
      "meetingUrl": "https://example.com",
      "metadata": {},
      "start": "string",
      "status": "string",
      "title": "string",
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Bookings action reference](actions/list-bookings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cal/latest/actions/list-bookings).

## Add Booking Attendee

Updates a booking in Cal.com by adding an attendee.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cal/latest/actions/add-booking-attendee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingUid": "string",
  "name": "Ava Chen",
  "timeZone": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cal/latest/actions/add-booking-attendee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingUid": "string",
    "name": "Ava Chen",
    "timeZone": "string",
    "email": "ava@example.com"
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
      "absent": true,
      "bookingId": 1,
      "displayEmail": "ava@example.com",
      "email": "ava@example.com",
      "id": 1,
      "language": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Booking Attendee action reference](actions/add-booking-attendee.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cal/latest/actions/add-booking-attendee).
