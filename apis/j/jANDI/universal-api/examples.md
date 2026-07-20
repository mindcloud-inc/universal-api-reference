# JANDI Universal API Examples

These examples use the MindCloud API key and JANDI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Incoming Webhook Message



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jANDI/latest/actions/send-incoming-webhook-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "MindCloud test message"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jANDI/latest/actions/send-incoming-webhook-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "MindCloud test message"
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

See the full [Send Incoming Webhook Message action reference](actions/send-incoming-webhook-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jANDI/latest/actions/send-incoming-webhook-message).
