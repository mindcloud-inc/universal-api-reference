# Yanado: List Comments

Retrieves comments from Yanado.

```
GET https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yanado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-comments?${params}`, {
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
| `listId` | string | no | Filter comments by list ID. |
| `query` | string | no | Search comments by query text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "assigneeName": "Ava Chen",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "listId": "string",
      "listName": "Ava Chen",
      "message": "string",
      "statusId": "string",
      "statusName": "Ava Chen",
      "taskCreated": "2026-05-07T12:00:00.000Z",
      "taskDescription": "string",
      "taskDueDate": "2026-05-07T12:00:00.000Z",
      "taskHighPriority": true,
      "taskId": "string",
      "taskName": "Ava Chen",
      "userId": "string",
      "userName": "Ava Chen"
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
| `created` | date | Comment creation time |
| `id` | string | Comment ID |
| `listId` | string | List ID |
| `listName` | string | List name |
| `message` | string | Comment message |
| `statusId` | string | Status ID |
| `statusName` | string | Status name |
| `taskCreated` | date | Task creation time |
| `taskDescription` | string | Task description |
| `taskDueDate` | date | Task due date |
| `taskHighPriority` | boolean | Whether the task is high priority |
| `taskId` | string | Task ID |
| `taskName` | string | Task name |
| `userId` | string | User ID |
| `userName` | string | User name |

## Native endpoint

Through the native Yanado API, this operation is `GET /public-api/comments` (base URL `https://api.yanado.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

