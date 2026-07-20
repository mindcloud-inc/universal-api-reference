# KeyVox Universal API Examples

These examples use the MindCloud API key and KeyVox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Units

Lists rooms and devices in your KeyVox account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-units?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-units?${params}`, {
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
      "placeName": "Ava Chen",
      "placeType": "string",
      "unitId": "string",
      "unitName": "Ava Chen",
      "unitState": "string",
      "unitType": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Units action reference](actions/list-units.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/keyVox/latest/actions/list-units).

## Check In Booking

Checks a booking in to KeyVox.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/check-in-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/check-in-booking', {
  method: 'PUT',
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
      "value": 1
    }
  ],
  "meta": {}
}
```

See the full [Check In Booking action reference](actions/check-in-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/keyVox/latest/actions/check-in-booking).
