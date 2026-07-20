# AppFit Universal API Examples

These examples use the MindCloud API key and AppFit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Track Metric Event

Creates a metric event in AppFit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appFit/latest/actions/track-metric-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "occurredAt": "2026-05-07T12:00:00.000Z",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appFit/latest/actions/track-metric-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "occurredAt": "2026-05-07T12:00:00.000Z",
    "payload": {}
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

See the full [Track Metric Event action reference](actions/track-metric-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/appFit/latest/actions/track-metric-event).
