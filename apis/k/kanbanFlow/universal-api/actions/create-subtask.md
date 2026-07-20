# KanbanFlow: Create subtask

Creates a new subtask in KanbanFlow.

```
POST https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/create-subtask
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/create-subtask" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/create-subtask', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The KanbanFlow task ID. |
| `name` | string | yes | The subtask name. |
| `finished` | boolean | no | Whether the subtask is complete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "insertIndex": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `insertIndex` | number |  |

## Native endpoint

Through the native KanbanFlow API, this operation is `POST /tasks/:taskId/subtasks` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subtask.md) for the provider-specific parameters and requirements.

