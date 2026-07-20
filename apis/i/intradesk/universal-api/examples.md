# Intradesk Universal API Examples

These examples use the MindCloud API key and Intradesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tasks

Retrieves tasks from Intradesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-tasks?${params}`, {
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
      "aiemotionalassessment": "string",
      "aihistory": "string",
      "customerid": 1,
      "description": "string",
      "id": 1,
      "initiator": 1,
      "name": "Ava Chen",
      "priority": 1,
      "prioritycriticality": 1,
      "priorityinfluence": 1,
      "status": 1,
      "tasknumber": 1
    }
  ],
  "meta": {}
}
```

See the full [List Tasks action reference](actions/list-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intradesk/latest/actions/list-tasks).

## Copy Task

Copies an existing task in Intradesk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/copy-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/copy-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
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
      "authorId": 1,
      "correlationId": "string",
      "data": {},
      "errorMessage": "string",
      "errorType": 1,
      "id": 1,
      "isSuccess": true,
      "message": "string",
      "messages": {},
      "number": 1,
      "taskProcessType": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Copy Task action reference](actions/copy-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intradesk/latest/actions/copy-task).
