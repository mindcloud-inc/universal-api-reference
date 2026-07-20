# Uchat Universal API Examples

These examples use the MindCloud API key and Uchat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Plugin Message

Sends an array-wrapped message payload to a Uchat plugin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uchat/latest/actions/send-plugin-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload[]": "123456789123",
  "pluginId": "youtube"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uchat/latest/actions/send-plugin-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload[]": "123456789123",
    "pluginId": "youtube"
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

See the full [Send Plugin Message action reference](actions/send-plugin-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uchat/latest/actions/send-plugin-message).
