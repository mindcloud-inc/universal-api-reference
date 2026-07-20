# KanbanFlow Universal API Examples

These examples use the MindCloud API key and KanbanFlow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get board

Retrieves the structure of a KanbanFlow board.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board?${params}`, {
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
      "colors": [
        {
          "name": "Ava Chen",
          "value": "string"
        }
      ],
      "columns": [
        {
          "name": "Ava Chen",
          "uniqueId": "string"
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get board action reference](actions/get-board.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kanbanFlow/latest/actions/get-board).

## Add comment

Creates a new comment on a KanbanFlow task.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "text": "string"
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
      "taskCommentId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kanbanFlow/latest/actions/add-comment).
