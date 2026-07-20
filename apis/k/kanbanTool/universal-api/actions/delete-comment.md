# Kanban Tool: Delete Comment



```
DELETE https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-comment?connectionId=$CONNECTION_ID&taskId=1&commentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1",
  "commentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-comment?${params}`, {
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
| `taskId` | number | yes | Parent task ID. |
| `commentId` | number | yes | Kanban Tool comment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentable_version": 1,
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentable_version` | number |  |
| `content` | string |  |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `id` | number |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native Kanban Tool API, this operation is `DELETE /tasks/:task_id/comments/:comment_id.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-comment.md) for the provider-specific parameters and requirements.

