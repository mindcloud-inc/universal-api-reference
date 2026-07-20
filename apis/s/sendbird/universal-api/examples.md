# Sendbird Universal API Examples

These examples use the MindCloud API key and Sendbird connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-users?${params}`, {
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
      "createdAt": 1,
      "isActive": true,
      "nickname": "Ava Chen",
      "profileUrl": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendbird/latest/actions/list-users).

## Accept Group Channel Invitation



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/accept-group-channel-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/accept-group-channel-invitation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelUrl": "https://example.com"
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
      "channelUrl": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Accept Group Channel Invitation action reference](actions/accept-group-channel-invitation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendbird/latest/actions/accept-group-channel-invitation).
