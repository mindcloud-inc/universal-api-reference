# Jostle Universal API Examples

These examples use the MindCloud API key and Jostle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Enterprise Users



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/list-enterprise-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jostle/latest/actions/list-enterprise-users?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Enterprise Users action reference](actions/list-enterprise-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jostle/latest/actions/list-enterprise-users).

## Attach File to Task Comment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/attach-file-to-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "commentId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jostle/latest/actions/attach-file-to-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "commentId": "string",
    "url": "https://example.com"
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
      "data": {},
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Attach File to Task Comment action reference](actions/attach-file-to-task-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jostle/latest/actions/attach-file-to-task-comment).
