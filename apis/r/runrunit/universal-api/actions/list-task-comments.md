# Runrun.it: List Task Comments

Retrieves comments for a task in Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-task-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-task-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-task-comments?${params}`, {
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
| `taskId` | string | yes | Task Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children_count": 1,
      "comment_id": "string",
      "commentable_id": 1,
      "commentable_type": "string",
      "commenter_name": "Ava Chen",
      "created_at": "string",
      "deleted_at": "string",
      "document_id": "string",
      "documents": [
        "string"
      ],
      "edited_at": "string",
      "enterprise_id": "string",
      "guest_id": "string",
      "id": 1,
      "is_automation_message": true,
      "is_legacy": true,
      "is_system_message": true,
      "media": "string",
      "quoted_comment_guest_id": "string",
      "quoted_comment_guest_name": "Ava Chen",
      "quoted_comment_id": "string",
      "quoted_comment_text": "string",
      "quoted_comment_user_id": "string",
      "quoted_comment_user_name": "Ava Chen",
      "reactions": [
        "string"
      ],
      "related_task_ids": "string",
      "task_id": 1,
      "team_id": "string",
      "text": "string",
      "thread_id": 1,
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children_count` | number |  |
| `comment_id` | string |  |
| `commentable_id` | number |  |
| `commentable_type` | string |  |
| `commenter_name` | string |  |
| `created_at` | string |  |
| `deleted_at` | string |  |
| `document_id` | string |  |
| `documents` | array<string> |  |
| `edited_at` | string |  |
| `enterprise_id` | string |  |
| `guest_id` | string |  |
| `id` | number |  |
| `is_automation_message` | boolean |  |
| `is_legacy` | boolean |  |
| `is_system_message` | boolean |  |
| `media` | string |  |
| `quoted_comment_guest_id` | string |  |
| `quoted_comment_guest_name` | string |  |
| `quoted_comment_id` | string |  |
| `quoted_comment_text` | string |  |
| `quoted_comment_user_id` | string |  |
| `quoted_comment_user_name` | string |  |
| `reactions` | array<string> |  |
| `related_task_ids` | string |  |
| `task_id` | number |  |
| `team_id` | string |  |
| `text` | string |  |
| `thread_id` | number |  |
| `user_id` | string |  |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /tasks/:task_id/comments` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-task-comments.md) for the provider-specific parameters and requirements.

