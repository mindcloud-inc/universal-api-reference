# SyncMate Universal API Examples

These examples use the MindCloud API key and SyncMate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Connection



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/check-connection?${params}`, {
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
      "data": {},
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Check Connection action reference](actions/check-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/syncMate/latest/actions/check-connection).

## Connect WhatsApp Session



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/connect-whats-app-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "5511999999999"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/connect-whats-app-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "5511999999999"
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
      "data": {},
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Connect WhatsApp Session action reference](actions/connect-whats-app-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/syncMate/latest/actions/connect-whats-app-session).
