# Kanban Tool: Update Task



```
PUT https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | Kanban Tool task ID. |
| `name` | string | no | Task title. Example: `Make Jenny a sandwich.`. |
| `assignedUserId` | number | no | User who should own the task. Example: `1000`. |
| `description` | string | no | Task description. HTML is supported. Example: `<p>And do it now!</p>`. |
| `priority` | number | no | Task priority: `-1` low, `0` normal, `1` high. Example: `1`. |
| `tags` | string | no | Comma-separated list of tags. Example: `bug,chrome,something-else`. |
| `dueDate` | date | no | Task due date. Example: `2026-03-31`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | number | no | Move the task to another board. Example: `100000`. |
| `workflowStageId` | number | no | Target workflow stage. Example: `200000`. |
| `swimlaneId` | number | no | Target swimlane. Example: `300000`. |
| `cardTypeId` | number | no | Card type to assign to the task. Example: `400000`. |
| `timeEstimate` | number | no | Estimated work in seconds. Example: `3600`. |
| `sizeEstimate` | string | no | Difficulty estimate string such as `1.0` or `5.0`. Example: `1.0`. |
| `postponedUntil` | date | no | Postpone the task until this date. Example: `2026-04-07`. |
| `position` | number | no | Task position inside the board cell. Example: `1`. |
| `externalId` | number | no | Custom external identifier for synchronization. Example: `673409`. |
| `externalLink` | string | no | Custom external URL for the task. Example: `https://docs.google.com/document/d/abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "position": 1,
      "priority": 1,
      "tags": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "workflow_stage_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `board_id` | number |  |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `position` | number |  |
| `priority` | number |  |
| `tags` | string |  |
| `updated_at` | date |  |
| `workflow_stage_id` | number |  |

## Native endpoint

Through the native Kanban Tool API, this operation is `PATCH /tasks/:task_id.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

