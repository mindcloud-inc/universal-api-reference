# ProveSource Universal API Examples

These examples use the MindCloud API key and ProveSource connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Webhook Event



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proveSource/latest/actions/send-webhook-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proveSource/latest/actions/send-webhook-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": "string"
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

See the full [Send Webhook Event action reference](actions/send-webhook-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proveSource/latest/actions/send-webhook-event).
