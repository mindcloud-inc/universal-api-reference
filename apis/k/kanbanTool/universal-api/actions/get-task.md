# Kanban Tool: Get Task



```
GET https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/get-task?${params}`, {
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
| `taskId` | number | yes | Kanban Tool task ID. |

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

Through the native Kanban Tool API, this operation is `GET /tasks/:task_id/preload.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

