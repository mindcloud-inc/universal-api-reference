# zipBoard: Delete Task

Deletes an existing task from zipBoard.

```
DELETE https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/delete-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/delete-task?${params}`, {
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
| `id` | string | yes | Task record ID to delete. |

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

Through the native zipBoard API, this operation is `DELETE /issues/tasks/:id` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

