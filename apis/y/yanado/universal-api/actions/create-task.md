# Yanado: Create Task

Creates a new task in Yanado.

```
POST https://connect.mindcloud.co/v1/universal/yanado/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yanado `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Yanado list ID where the task should be created. |
| `name` | string | yes | Task name. |
| `statusId` | string | yes | Yanado status ID for the new task. |
| `assigneeId` | string | no | Assign the new task to this user ID. |
| `description` | string | no | Task description. |
| `dueDate` | date | no | Task due date. |
| `form` | object | no | Additional task form payload. |
| `threadEmail` | string | no | Participant email for the thread. |
| `threadId` | string | no | Thread ID. |
| `threadName` | string | no | Thread name. |
| `threadSubject` | string | no | Thread subject. |

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

Through the native Yanado API, this operation is `POST /public-api/tasks` (base URL `https://api.yanado.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

