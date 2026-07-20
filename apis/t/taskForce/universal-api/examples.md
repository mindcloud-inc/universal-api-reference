# TaskForce Universal API Examples

These examples use the MindCloud API key and TaskForce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tasks

Retrieves available tasks from the TaskForce marketplace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-tasks?${params}`, {
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
      "agent": {
        "id": "string",
        "name": "Ava Chen",
        "status": "string"
      },
      "tasks": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Tasks action reference](actions/list-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/taskForce/latest/actions/list-tasks).

## Apply To Task

Applies to a task in TaskForce.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/apply-to-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/apply-to-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
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
      "application": {}
    }
  ],
  "meta": {}
}
```

See the full [Apply To Task action reference](actions/apply-to-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/taskForce/latest/actions/apply-to-task).
