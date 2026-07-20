# Yanado: Update Task

Updates an existing task in Yanado.

```
PUT https://connect.mindcloud.co/v1/universal/yanado/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yanado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yanado/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yanado/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Yanado task ID. |
| `archived` | boolean | no | Archive state for the task. |
| `assigneeId` | string | no | Assign the task to this user ID. |
| `description` | string | no | Task description. |
| `dueDate` | date | no | Task due date. |
| `form` | object | no | Additional task form payload. |
| `listId` | string | no | Yanado list ID for the task. |
| `name` | string | no | Task name. |
| `statusId` | string | no | Yanado status ID for the task. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | string | Assignee ID |
| `assigneeName` | string | Assignee name |
| `createTime` | date | Task creation time |
| `description` | string | Task description |
| `dueDate` | date | Task due date |
| `highPriority` | boolean | Whether the task is high priority |
| `listId` | string | List ID |
| `listName` | string | List name |
| `name` | string | Task name |
| `statusId` | string | Status ID |
| `statusName` | string | Status name |
| `taskId` | string | Task ID |

## Native endpoint

Through the native Yanado API, this operation is `PUT /public-api/tasks/:taskId` (base URL `https://api.yanado.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

