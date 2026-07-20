# Wbiztool Universal API Examples

These examples use the MindCloud API key and Wbiztool connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Credentials

Checks whether your Wbiztool credentials are valid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/check-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/check-credentials?${params}`, {
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
      "message": "string",
      "name": "Ava Chen",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Check Credentials action reference](actions/check-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wbiztool/latest/actions/check-credentials).

## Connect WhatsApp Number

Connects a WhatsApp account in Wbiztool.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/connect-whats-app-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/connect-whats-app-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "string"
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
      "message": "string",
      "status": 1,
      "whatsappClientId": 1
    }
  ],
  "meta": {}
}
```

See the full [Connect WhatsApp Number action reference](actions/connect-whats-app-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wbiztool/latest/actions/connect-whats-app-number).
