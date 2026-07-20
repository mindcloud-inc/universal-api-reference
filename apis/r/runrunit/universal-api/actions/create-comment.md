# Runrun.it: Create Comment

Creates a new comment in Runrun.it.

```
POST https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | Task ID to comment on. |
| `text` | string | yes | Comment text. |

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

Through the native Runrun.it API, this operation is `POST /comments` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

