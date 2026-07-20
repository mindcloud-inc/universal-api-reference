# PingBell Universal API Examples

These examples use the MindCloud API key and PingBell connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List PingBells

Retrieves PingBells from your PingBell account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/list-pingbells?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/list-pingbells?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List PingBells action reference](actions/list-pingbells.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pingBell/latest/actions/list-pingbells).

## Send Notification

Creates a notification for a specific PingBell.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pingbellId": "FyUlzEhej6gW0XAUmgL6"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pingbellId": "FyUlzEhej6gW0XAUmgL6"
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

See the full [Send Notification action reference](actions/send-notification.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pingBell/latest/actions/send-notification).
