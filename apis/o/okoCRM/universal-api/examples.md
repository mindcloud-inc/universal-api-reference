# OkoCRM Universal API Examples

These examples use the MindCloud API key and OkoCRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List users

Retrieves users from OkoCRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-users?${params}`, {
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
      "act": 1,
      "avatar_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date_born": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "last_visit": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/okoCRM/latest/actions/list-users).

## Complete task with comment

Marks a task as done in OkoCRM with a comment.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/complete-task-with-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/complete-task-with-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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
      "result": 1
    }
  ],
  "meta": {}
}
```

See the full [Complete task with comment action reference](actions/complete-task-with-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/okoCRM/latest/actions/complete-task-with-comment).
