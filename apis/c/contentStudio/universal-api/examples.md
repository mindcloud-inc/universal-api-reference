# ContentStudio Universal API Examples

These examples use the MindCloud API key and ContentStudio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from ContentStudio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/get-authenticated-user?${params}`, {
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
      "authenticatedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateFormat": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "fullName": "Ava Chen",
      "Id": "string",
      "image": "string",
      "lastname": "Chen",
      "phoneNo": "string",
      "state": "string",
      "timeFormat": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contentStudio/latest/actions/get-authenticated-user).

## Add Comment to Post

Adds a comment or internal note to a ContentStudio post.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/add-comment-to-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "comment": "string",
  "post_id": "string",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/add-comment-to-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "comment": "string",
    "post_id": "string",
    "workspace_id": "string"
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
      "author": {},
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "isNote": true,
      "mentionedUsers": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Comment to Post action reference](actions/add-comment-to-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contentStudio/latest/actions/add-comment-to-post).
