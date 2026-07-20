# Google Tasks Universal API Examples

These examples use the MindCloud API key and Google Tasks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Task Lists

Finds task lists in Google Tasks.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-task-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-task-lists?${params}`, {
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
      "etag": "string",
      "id": "string",
      "kind": "string",
      "selfLink": "https://example.com",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Task Lists action reference](actions/list-task-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleTasks/latest/actions/list-task-lists).

## Create Task

Creates a new task in Google Tasks.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasklist": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tasklist": "string"
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
      "etag": "string",
      "id": "string",
      "kind": "string",
      "notes": "string",
      "position": "string",
      "selfLink": "https://example.com",
      "status": "string",
      "title": "string",
      "updated": "string",
      "webViewLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Task action reference](actions/create-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleTasks/latest/actions/create-task).
