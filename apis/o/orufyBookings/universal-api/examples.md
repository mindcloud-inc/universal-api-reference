# Orufy Bookings Universal API Examples

These examples use the MindCloud API key and Orufy Bookings connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/list-events?${params}`, {
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
      "appInfo": {},
      "events": [
        {}
      ],
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orufyBookings/latest/actions/list-events).

## Cancel Booking



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/cancel-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attendeeId": "string",
  "meetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/cancel-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attendeeId": "string",
    "meetId": "string"
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
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

See the full [Cancel Booking action reference](actions/cancel-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orufyBookings/latest/actions/cancel-booking).
