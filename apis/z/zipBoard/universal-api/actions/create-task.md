# zipBoard: Create Task

Creates a new task in zipBoard.

```
POST https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional task description. |
| `priority` | string | no | Optional task priority. |
| `projectId` | string | yes | Project ID where the task should be created. |
| `status` | string | no | Optional task status. |
| `title` | string | yes | Task title. |
| `type` | string | no | Optional task type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": "string",
      "commentText": "string",
      "commentType": "string",
      "project_id": "string",
      "taskId": "string",
      "taskPriority": "string",
      "taskStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | string | Comment identifier. |
| `commentText` | string | Task text. |
| `commentType` | string | Comment type. |
| `project_id` | string | Project identifier. |
| `taskId` | string | Task identifier. |
| `taskPriority` | string | Task priority. |
| `taskStatus` | string | Task status. |

## Native endpoint

Through the native zipBoard API, this operation is `POST /issues/tasks` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

