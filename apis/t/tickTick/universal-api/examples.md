# TickTick Universal API Examples

These examples use the MindCloud API key and TickTick connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List User Projects

Retrieves the user's projects from TickTick.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/list-user-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/list-user-projects?${params}`, {
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
      "closed": true,
      "color": "string",
      "groupId": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "permission": "string",
      "sortOrder": 1,
      "viewMode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List User Projects action reference](actions/list-user-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tickTick/latest/actions/list-user-projects).

## Complete Task

Marks a task as complete in TickTick.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/complete-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/complete-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "taskId": "string"
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
      "projectId": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Complete Task action reference](actions/complete-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tickTick/latest/actions/complete-task).
