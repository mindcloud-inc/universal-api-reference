# Loggly (Send Data) Universal API Examples

These examples use the MindCloud API key and Loggly (Send Data) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Bulk Events

Creates bulk log events in Loggly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-bulk-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerToken": "123e4567-e89b-12d3-a456-426614174000",
  "tagPath": "app/server",
  "events": "first event line\\nsecond event line"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-bulk-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerToken": "123e4567-e89b-12d3-a456-426614174000",
    "tagPath": "app/server",
    "events": "first event line\\nsecond event line"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Bulk Events action reference](actions/send-bulk-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logglySendData/latest/actions/send-bulk-events).
