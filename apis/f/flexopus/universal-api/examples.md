# Flexopus Universal API Examples

These examples use the MindCloud API key and Flexopus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Buildings

Retrieves a list of buildings from Flexopus.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-buildings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-buildings?${params}`, {
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
        {
          "address": "string",
          "id": 1,
          "locations": [
            {
              "code": "string",
              "id": 1,
              "name": "Ava Chen"
            }
          ],
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Buildings action reference](actions/list-buildings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flexopus/latest/actions/list-buildings).

## Create Booking

Creates a new booking in Flexopus.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookableId": 1,
  "toTime": "2026-05-07T12:00:00.000Z",
  "userId": 1,
  "locationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookableId": 1,
    "toTime": "2026-05-07T12:00:00.000Z",
    "userId": 1,
    "locationId": 1
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
      "data": [
        {
          "bookable": {
            "id": 1,
            "name": "Ava Chen",
            "status": 1,
            "type": 1
          },
          "from": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "livemap": "string",
          "to": "2026-05-07T12:00:00.000Z",
          "user": {
            "email": "ava@example.com",
            "extensionAttributes": {},
            "id": 1,
            "name": "Ava Chen"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Booking action reference](actions/create-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flexopus/latest/actions/create-booking).
