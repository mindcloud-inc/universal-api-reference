# Yanado Universal API Examples

These examples use the MindCloud API key and Yanado connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users From Team

Retrieves users from a Yanado team.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-users-from-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-users-from-team?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Users From Team action reference](actions/list-users-from-team.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yanado/latest/actions/list-users-from-team).

## Create Task

Creates a new task in Yanado.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yanado/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "name": "Ava Chen",
  "statusId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yanado/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "name": "Ava Chen",
    "statusId": "string"
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
      "assigneeId": "string",
      "assigneeName": "Ava Chen",
      "createTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "highPriority": true,
      "listId": "string",
      "listName": "Ava Chen",
      "name": "Ava Chen",
      "statusId": "string",
      "statusName": "Ava Chen",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Task action reference](actions/create-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yanado/latest/actions/create-task).
