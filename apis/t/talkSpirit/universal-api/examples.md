# talkSpirit Universal API Examples

These examples use the MindCloud API key and talkSpirit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Post

Creates a new post in talkSpirit via incoming webhook.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talkSpirit/latest/actions/send-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talkSpirit/latest/actions/send-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
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
      "content": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Post action reference](actions/send-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/talkSpirit/latest/actions/send-post).
