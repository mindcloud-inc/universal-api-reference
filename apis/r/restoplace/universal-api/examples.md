# Restoplace Universal API Examples

These examples use the MindCloud API key and Restoplace connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Address Info

Retrieves address information from Restoplace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/get-address-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/get-address-info?${params}`, {
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

See the full [Get Address Info action reference](actions/get-address-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/restoplace/latest/actions/get-address-info).

## Create Reservation

Creates a new reservation in Restoplace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/create-reservation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/create-reservation', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Reservation action reference](actions/create-reservation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/restoplace/latest/actions/create-reservation).
