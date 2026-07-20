# Yanado: Get Task

Retrieves a task from Yanado.

```
GET https://connect.mindcloud.co/v1/universal/yanado/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yanado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yanado/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yanado/latest/actions/get-task?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Yanado task ID. |

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

Through the native Yanado API, this operation is `GET /public-api/tasks/:taskId` (base URL `https://api.yanado.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

