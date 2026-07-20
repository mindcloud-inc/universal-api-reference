# BlogIn Universal API Examples

These examples use the MindCloud API key and BlogIn connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Members

Retrieves all members from BlogIn.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-members?${params}`, {
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
      "access_level": "string",
      "avatar": "string",
      "email": "ava@example.com",
      "id": 1,
      "job_title": "string",
      "name": "Ava Chen",
      "phone": "string",
      "status": "string",
      "surname": "Ava Chen",
      "teams": [
        {}
      ],
      "time_registered": "string",
      "timezone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Members action reference](actions/list-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blogIn/latest/actions/list-members).

## Add Post Comment

Adds a comment to a BlogIn post.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/add-post-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "text": "string",
  "author.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/add-post-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "text": "string",
    "author.id": 1
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
      "approved": true,
      "approved_at": "string",
      "author": {},
      "created_at": "string",
      "id": 1,
      "parent": 1,
      "text": "string",
      "votes_down": 1,
      "votes_up": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Post Comment action reference](actions/add-post-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blogIn/latest/actions/add-post-comment).
