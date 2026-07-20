# Morf Universal API Examples

These examples use the MindCloud API key and Morf connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Track Event

Sends a track event to Morf.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morf/latest/actions/send-track-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_name": "Ava Chen",
  "user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morf/latest/actions/send-track-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_name": "Ava Chen",
    "user_id": "string"
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
      "status_code": 1
    }
  ],
  "meta": {}
}
```

See the full [Send Track Event action reference](actions/send-track-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/morf/latest/actions/send-track-event).
