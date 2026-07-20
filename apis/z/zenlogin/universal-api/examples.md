# Zenlogin Universal API Examples

These examples use the MindCloud API key and Zenlogin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create Login Check



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenlogin/latest/actions/create-login-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identityKey": "usr12345",
  "identityEmailAddress": "name@example.com",
  "userAgent": "Mozilla/5.0",
  "ipAddress": "20.169.78.172"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenlogin/latest/actions/create-login-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identityKey": "usr12345",
    "identityEmailAddress": "name@example.com",
    "userAgent": "Mozilla/5.0",
    "ipAddress": "20.169.78.172"
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
      "data": {
        "email_notification_sent": 1,
        "id": "string",
        "status_key": "string",
        "timestamp": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Login Check action reference](actions/create-login-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zenlogin/latest/actions/create-login-check).
