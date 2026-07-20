# Makeplans Universal API Examples

These examples use the MindCloud API key and Makeplans connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Services

Retrieves services from Makeplans.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-services?${params}`, {
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
      "active": true,
      "booking_type": "string",
      "description": "string",
      "id": 1,
      "interval": 1,
      "price": 1,
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Services action reference](actions/list-services.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/makeplans/latest/actions/list-services).

## Cancel Booking

Cancels an existing booking in Makeplans.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/cancel-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/cancel-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingId": 1
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
      "active": true,
      "booked_from": "2026-05-07T12:00:00.000Z",
      "booked_to": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "state": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Booking action reference](actions/cancel-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/makeplans/latest/actions/cancel-booking).
