# Luxafor Universal API Examples

These examples use the MindCloud API key and Luxafor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Blink Device

Updates a Luxafor device by blinking it.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/blink-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionFields.color": "red"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/blink-device', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionFields.color": "red"
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

See the full [Blink Device action reference](actions/blink-device.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/luxafor/latest/actions/blink-device).
