# Walls.io Universal API Examples

These examples use the MindCloud API key and Walls.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Posts

Retrieves posts from Walls.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/list-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/list-posts?${params}`, {
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
      "count": 1,
      "current_time": 1,
      "data": [
        {}
      ],
      "info": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Posts action reference](actions/list-posts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wallsio/latest/actions/list-posts).

## Clear Post Spam

Clears a post spam status in Walls.io.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/clear-post-spam" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/clear-post-spam', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "current_time": 1,
      "data": {},
      "info": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Clear Post Spam action reference](actions/clear-post-spam.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wallsio/latest/actions/clear-post-spam).
