# GanttPRO: Create Task Comment

Creates a new comment on a GanttPRO task.

```
POST https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1,
  "userId": 1,
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1,
    "userId": 1,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | Task identifier for the new comment. |
| `userId` | number | yes | User identifier for the comment author. |
| `content` | string | yes | Comment content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "comment": "string",
        "content": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "is_removed": 1,
        "projectId": 1,
        "taskId": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "user": {},
        "userId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item.comment` | string |  |
| `item.content` | string |  |
| `item.createdAt` | date |  |
| `item.id` | number |  |
| `item.is_removed` | number |  |
| `item.projectId` | number |  |
| `item.taskId` | number |  |
| `item.updatedAt` | date |  |
| `item.user` | object |  |
| `item.userId` | number |  |

## Native endpoint

Through the native GanttPRO API, this operation is `POST /comments` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-comment.md) for the provider-specific parameters and requirements.

