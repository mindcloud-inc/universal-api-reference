# EventLogCentral Universal API Examples

These examples use the MindCloud API key and EventLogCentral connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Log Event

Creates an event in EventLogCentral.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventLogCentral/latest/actions/log-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventLogCentral/latest/actions/log-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
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
      "ok": true
    }
  ],
  "meta": {}
}
```

See the full [Log Event action reference](actions/log-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventLogCentral/latest/actions/log-event).
