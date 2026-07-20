# Hook.Notifier Universal API Examples

These examples use the MindCloud API key and Hook.Notifier connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Notification

Sends a custom notification through Hook.Notifier.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hookNotifier/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hookNotifier/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": "string",
    "body": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Notification action reference](actions/send-notification.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hookNotifier/latest/actions/send-notification).
