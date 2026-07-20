# Edoobox Universal API Examples

These examples use the MindCloud API key and Edoobox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Booking

Retrieves details for a booking from Edoobox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-booking?connectionId=$CONNECTION_ID&bookingId=booking_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "booking_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-booking?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Booking action reference](actions/get-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/edoobox/latest/actions/get-booking).

## Cancel Booking

Cancels an existing booking in Edoobox.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/cancel-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": "booking_example",
  "offer": "offer_ac159e317af1_7511348589"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/cancel-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingId": "booking_example",
    "offer": "offer_ac159e317af1_7511348589"
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
      "cancel": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Booking action reference](actions/cancel-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/edoobox/latest/actions/cancel-booking).
