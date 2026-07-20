# FleetWire Universal API Examples

These examples use the MindCloud API key and FleetWire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bookings

Retrieves bookings from FleetWire.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/list-bookings?${params}`, {
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
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [List Bookings action reference](actions/list-bookings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fleetWire/latest/actions/list-bookings).

## Create Booking

Creates a new booking in FleetWire.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "version": "v2",
  "listingId": "string",
  "start": "string",
  "end": "string",
  "customerFirstName": "Ava",
  "customerLastName": "Chen",
  "customerEmail": "ava@example.com",
  "customerPhone": "string",
  "isPrimaryCustomer": true,
  "customerPhoneNumber": "string",
  "agreeToTerms": true,
  "customerDob": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "version": "v2",
    "listingId": "string",
    "start": "string",
    "end": "string",
    "customerFirstName": "Ava",
    "customerLastName": "Chen",
    "customerEmail": "ava@example.com",
    "customerPhone": "string",
    "isPrimaryCustomer": true,
    "customerPhoneNumber": "string",
    "agreeToTerms": true,
    "customerDob": "string"
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
      "b_id": "string",
      "customer": {},
      "l_id": "string",
      "p_id": "string",
      "stripePaymentIntent": {},
      "stripeSession": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Booking action reference](actions/create-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fleetWire/latest/actions/create-booking).
