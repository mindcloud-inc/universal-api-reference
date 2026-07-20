# Stream Universal API Examples

These examples use the MindCloud API key and Stream connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App Settings

Retrieves app settings from Stream.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stream/latest/actions/get-app-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stream/latest/actions/get-app-settings?${params}`, {
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
      "app": {},
      "duration": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get App Settings action reference](actions/get-app-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stream/latest/actions/get-app-settings).

## Ban User

Bans a user in Stream.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stream/latest/actions/ban-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUserId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stream/latest/actions/ban-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUserId": "string",
    "userId": "string"
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
      "duration": "string"
    }
  ],
  "meta": {}
}
```

See the full [Ban User action reference](actions/ban-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stream/latest/actions/ban-user).
