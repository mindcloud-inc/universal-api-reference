# Lodgify Universal API Examples

These examples use the MindCloud API key and Lodgify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Properties

Retrieves a list of properties from Lodgify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-properties?${params}`, {
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
      "address": "string",
      "city": "string",
      "contact": {},
      "country": "string",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "description": "string",
      "hasAddons": true,
      "hasAgreement": true,
      "hideAddress": true,
      "id": 1,
      "imageUrl": "https://example.com",
      "inOutMaxDate": "2026-05-07T12:00:00.000Z",
      "internalName": "Ava Chen",
      "isActive": true,
      "latitude": 1,
      "longitude": 1,
      "maxPrice": 1,
      "minPrice": 1,
      "name": "Ava Chen",
      "originalMaxPrice": 1,
      "originalMinPrice": 1,
      "priceUnitInDays": 1,
      "rating": 1,
      "rooms": [
        {}
      ],
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Properties action reference](actions/list-properties.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lodgify/latest/actions/list-properties).

## Update Reservation Status

Updates a booking's status in Lodgify.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/update-reservation-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reservationId": "19199854",
  "statusAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/update-reservation-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reservationId": "19199854",
    "statusAction": "string"
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

See the full [Update Reservation Status action reference](actions/update-reservation-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lodgify/latest/actions/update-reservation-status).
