# JmpTo Universal API Examples

These examples use the MindCloud API key and JmpTo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from JmpTo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-account?${params}`, {
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
      "avatar": "string",
      "email": "ava@example.com",
      "expires": "string",
      "id": 1,
      "planid": 1,
      "registered": "string",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jmpTo/latest/actions/get-account).

## Assign Item to Channel

Assigns an item to a channel in JmpTo.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/assign-item-to-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": 1,
  "type": "string",
  "itemId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/assign-item-to-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": 1,
    "type": "string",
    "itemId": 1
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
      "error": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assign Item to Channel action reference](actions/assign-item-to-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jmpTo/latest/actions/assign-item-to-channel).
