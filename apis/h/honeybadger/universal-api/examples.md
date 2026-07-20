# Honeybadger Universal API Examples

These examples use the MindCloud API key and Honeybadger connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping Check-in

Reports a check-in to Honeybadger by ID.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkInId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkInId": "string"
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

See the full [Ping Check-in action reference](actions/ping-check-in.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/honeybadger/latest/actions/ping-check-in).
