# Yanado: List Tasks With Emails Attached

Retrieves tasks with attached emails from Yanado.

```
GET https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-tasks-with-emails-attached
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yanado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-tasks-with-emails-attached?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-tasks-with-emails-attached?${params}`, {
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
| `listId` | string | no | Filter tasks by list ID. |
| `assignee` | string | no | Filter tasks by assignee. |
| `statusId` | string | no | Filter tasks by status ID. |
| `query` | string | no | Search tasks by query text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "assigneeName": "Ava Chen",
      "id": 1,
      "listId": "string",
      "listName": "Ava Chen",
      "participantEmail": "ava@example.com",
      "participantName": "Ava Chen",
      "statusId": "string",
      "statusName": "Ava Chen",
      "subject": "string",
      "taskCreated": "2026-05-07T12:00:00.000Z",
      "taskDescription": "string",
      "taskDueDate": "2026-05-07T12:00:00.000Z",
      "taskHighPriority": true,
      "taskId": "string",
      "taskName": "Ava Chen",
      "threadId": "string"
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
| `id` | number | Email task ID |
| `listId` | string | List ID |
| `listName` | string | List name |
| `participantEmail` | string | Participant email |
| `participantName` | string | Participant name |
| `statusId` | string | Status ID |
| `statusName` | string | Status name |
| `subject` | string | Email subject |
| `taskCreated` | date | Task creation time |
| `taskDescription` | string | Task description |
| `taskDueDate` | date | Task due date |
| `taskHighPriority` | boolean | Whether the task is high priority |
| `taskId` | string | Task ID |
| `taskName` | string | Task name |
| `threadId` | string | Thread ID |

## Native endpoint

Through the native Yanado API, this operation is `GET /public-api/email-tasks` (base URL `https://api.yanado.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks-with-emails-attached.md) for the provider-specific parameters and requirements.

