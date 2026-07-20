# Kanban Tool: Delete Subtask



```
DELETE https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-subtask
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-subtask?connectionId=$CONNECTION_ID&subtaskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subtaskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-subtask?${params}`, {
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
| `subtaskId` | number | yes | Kanban Tool subtask ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned_user_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by_id": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_completed": true,
      "name": "Ava Chen",
      "position": 1,
      "task_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned_user_id` | number |  |
| `created_at` | date |  |
| `created_by_id` | number |  |
| `deleted_at` | date |  |
| `id` | number |  |
| `is_completed` | boolean |  |
| `name` | string |  |
| `position` | number |  |
| `task_id` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Kanban Tool API, this operation is `DELETE /subtasks/:subtask_id.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subtask.md) for the provider-specific parameters and requirements.

