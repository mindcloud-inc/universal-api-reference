# Tallyfy: List Tasks

Retrieves tasks across your Tallyfy organization.

```
GET https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tallyfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_guest_owners": true,
      "can_complete_only_assignees": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "deadline": "2026-05-07T12:00:00.000Z",
      "everyone_must_complete": true,
      "has_deadline_dependent_child_tasks": true,
      "id": "string",
      "increment_id": 1,
      "is_completable": true,
      "is_oneoff_task": true,
      "is_soft_start_date": true,
      "last_updated": "2026-05-07T12:00:00.000Z",
      "max_assignable": 1,
      "original_title": "string",
      "owners": {
        "guests": [
          "string"
        ],
        "taskUrls": [
          "https://example.com"
        ],
        "users": [
          1
        ]
      },
      "position": 1,
      "prevent_guest_comment": true,
      "problem": true,
      "started_at": "2026-05-07T12:00:00.000Z",
      "starter_id": 1,
      "status": "string",
      "status_label": "string",
      "task_type": "string",
      "title": "string",
      "top_secret": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_guest_owners` | boolean |  |
| `can_complete_only_assignees` | boolean |  |
| `created_at` | date |  |
| `deadline` | date |  |
| `everyone_must_complete` | boolean |  |
| `has_deadline_dependent_child_tasks` | boolean |  |
| `id` | string |  |
| `increment_id` | number |  |
| `is_completable` | boolean |  |
| `is_oneoff_task` | boolean |  |
| `is_soft_start_date` | boolean |  |
| `last_updated` | date |  |
| `max_assignable` | number |  |
| `original_title` | string |  |
| `owners.guests[]` | string |  |
| `owners.taskUrls[]` | string |  |
| `owners.users[]` | number |  |
| `position` | number |  |
| `prevent_guest_comment` | boolean |  |
| `problem` | boolean |  |
| `started_at` | date |  |
| `starter_id` | number |  |
| `status` | string |  |
| `status_label` | string |  |
| `task_type` | string |  |
| `title` | string |  |
| `top_secret` | boolean |  |

## Native endpoint

Through the native Tallyfy API, this operation is `GET /organizations/:org/tasks` (base URL `https://api.tallyfy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

