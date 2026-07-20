# LoginRadius Universal API Examples

These examples use the MindCloud API key and LoginRadius connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Server Time

Retrieves current server time from LoginRadius.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/get-server-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/get-server-time?${params}`, {
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
      "currentTime": "string",
      "serverLocation": "string",
      "serverName": "Ava Chen",
      "sott": {
        "endTime": "string",
        "forWardedIP": "string",
        "ip": "string",
        "startTime": "string",
        "timeDifference": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Server Time action reference](actions/get-server-time.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loginRadius/latest/actions/get-server-time).

## Add Email

Adds an email address to a LoginRadius account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/add-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessToken": "Access token",
  "email": "alias@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/add-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessToken": "Access token",
    "email": "alias@example.com"
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
      "IsPosted": true
    }
  ],
  "meta": {}
}
```

See the full [Add Email action reference](actions/add-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loginRadius/latest/actions/add-email).
