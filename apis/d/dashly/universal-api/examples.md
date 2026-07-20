# Dashly Universal API Examples

These examples use the MindCloud API key and Dashly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Channels

Retrieves channels from a Dashly app.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/list-channels?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashly/latest/actions/list-channels?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Channels action reference](actions/list-channels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dashly/latest/actions/list-channels).

## Add Conversation Tag

Adds a tag to a Dashly conversation.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/add-conversation-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashly/latest/actions/add-conversation-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "tag": "string"
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

See the full [Add Conversation Tag action reference](actions/add-conversation-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dashly/latest/actions/add-conversation-tag).
