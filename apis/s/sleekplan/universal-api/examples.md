# Sleekplan Universal API Examples

These examples use the MindCloud API key and Sleekplan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Updates



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-updates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-updates?${params}`, {
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
      "announcement": true,
      "canDelete": true,
      "canEdit": true,
      "changelogId": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "draft": true,
      "feedbackId": 1,
      "productId": 1,
      "scheduled": true,
      "segment": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Updates action reference](actions/list-updates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sleekplan/latest/actions/list-updates).

## Create Comment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postId": "string"
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
      "commentId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Comment action reference](actions/create-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sleekplan/latest/actions/create-comment).
