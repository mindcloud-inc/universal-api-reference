# Zoho Cliq Universal API Examples

These examples use the MindCloud API key and Zoho Cliq connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Current Status

Retrieves the current user status from Zoho Cliq.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-current-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-current-status?${params}`, {
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
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Current Status action reference](actions/retrieve-current-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCliq/latest/actions/retrieve-current-status).

## Add Channel Members

Adds members to a Zoho Cliq channel.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/add-channel-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "userIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/add-channel-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "userIds[]": ["string"]
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

See the full [Add Channel Members action reference](actions/add-channel-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCliq/latest/actions/add-channel-members).
