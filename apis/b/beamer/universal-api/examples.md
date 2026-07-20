# Beamer Universal API Examples

These examples use the MindCloud API key and Beamer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Post Comments

Retrieves a post comment count from Beamer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/count-post-comments?connectionId=$CONNECTION_ID&postId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beamer/latest/actions/count-post-comments?${params}`, {
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

See the full [Count Post Comments action reference](actions/count-post-comments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beamer/latest/actions/count-post-comments).

## Create Post

Creates a new post in Beamer.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title[]": [
    "string"
  ],
  "content[]": [
    "string"
  ],
  "category": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beamer/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title[]": ["string"],
    "content[]": ["string"],
    "category": "string"
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

See the full [Create Post action reference](actions/create-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beamer/latest/actions/create-post).
