# Zoom Team Chat Universal API Examples

These examples use the MindCloud API key and Zoom Team Chat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List User's Channels



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-user-channels?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=me" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "me"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-user-channels?${params}`, {
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
      "channel_settings": {},
      "channel_url": "https://example.com",
      "id": "string",
      "jid": "string",
      "name": "Ava Chen",
      "type": 1
    }
  ],
  "meta": {}
}
```

See the full [List User's Channels action reference](actions/list-user-channels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zoomTeamChat/latest/actions/list-user-channels).

## Add Channel Members To A Mention Group



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/add-channel-members-to-a-mention-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "mentionGroupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/add-channel-members-to-a-mention-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "mentionGroupId": "string"
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

See the full [Add Channel Members To A Mention Group action reference](actions/add-channel-members-to-a-mention-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zoomTeamChat/latest/actions/add-channel-members-to-a-mention-group).
