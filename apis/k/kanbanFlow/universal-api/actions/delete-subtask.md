# KanbanFlow: Delete subtask

Deletes an existing subtask from KanbanFlow.

```
DELETE https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/delete-subtask
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/delete-subtask?connectionId=$CONNECTION_ID&taskId=string&index=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string",
  "index": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/delete-subtask?${params}`, {
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
| `taskId` | string | yes | The KanbanFlow task ID. |
| `index` | number | yes | The zero-based subtask index. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KanbanFlow API returns.

## Native endpoint

Through the native KanbanFlow API, this operation is `DELETE /tasks/:taskId/subtasks/by-index/:index` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subtask.md) for the provider-specific parameters and requirements.

