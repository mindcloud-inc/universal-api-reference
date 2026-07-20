# TikTok Conversions Universal API Examples

These examples use the MindCloud API key and TikTok Conversions connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Batch Offline Events

Reports offline events in bulk to TikTok Conversions.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-offline-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_set_id": "string",
  "batch[].event": "string",
  "batch[].timestamp": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-offline-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_set_id": "string",
    "batch[].event": "string",
    "batch[].timestamp": 1
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
      "code": 1,
      "data": {},
      "message": "string",
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Batch Offline Events action reference](actions/batch-offline-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tikTokConversions/latest/actions/batch-offline-events).
