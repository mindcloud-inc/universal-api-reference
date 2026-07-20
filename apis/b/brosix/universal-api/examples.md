# Brosix Universal API Examples

These examples use the MindCloud API key and Brosix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Message

Creates a new message in Brosix for a user or chat room.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brosix/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "MindCloud test message"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brosix/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "MindCloud test message"
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
      "result": 1
    }
  ],
  "meta": {}
}
```

See the full [Send Message action reference](actions/send-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brosix/latest/actions/send-message).
