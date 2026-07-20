# Awork: Set Task Assignees

Updates task assignees in Awork.

```
PUT https://connect.mindcloud.co/v1/universal/awork/latest/actions/set-task-assignees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/awork/latest/actions/set-task-assignees" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "userIds[]": "4ac8d1d3-64ca-4db7-b7e5-32226661cd76"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/awork/latest/actions/set-task-assignees', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "userIds[]": "4ac8d1d3-64ca-4db7-b7e5-32226661cd76"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The id of the task. |
| `userIds[]` | array<string> | yes | Array of user IDs to assign to the task. This replaces the existing assignee list. Example: `4ac8d1d3-64ca-4db7-b7e5-32226661cd76`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Awork API returns.

## Native endpoint

Through the native Awork API, this operation is `POST /tasks/:taskId/setassignees` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-task-assignees.md) for the provider-specific parameters and requirements.

