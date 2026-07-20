# KanbanFlow: Update label

Updates an existing label on a KanbanFlow task.

```
PUT https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/update-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/update-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "labelName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/update-label', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "labelName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The KanbanFlow task ID. |
| `labelName` | string | yes | The current label name. |
| `name` | string | no | The updated label name. |
| `pinned` | boolean | no | Whether the label should be pinned. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KanbanFlow API returns.

## Native endpoint

Through the native KanbanFlow API, this operation is `POST /tasks/:taskId/labels/by-name/:labelName` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-label.md) for the provider-specific parameters and requirements.

