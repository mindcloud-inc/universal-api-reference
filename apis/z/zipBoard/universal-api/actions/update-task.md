# zipBoard: Update Task

Updates an existing task in zipBoard.

```
PUT https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Updated task description. |
| `id` | string | yes | Task record ID to update. |
| `priority` | string | no | Updated task priority. |
| `status` | string | no | Updated task status. |
| `title` | string | no | Updated task title. |
| `type` | string | no | Updated task type. |

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

Through the native zipBoard API, this operation is `PUT /issues/tasks/:id` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

