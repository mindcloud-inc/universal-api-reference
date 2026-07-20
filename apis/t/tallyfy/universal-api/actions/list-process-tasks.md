# Tallyfy: List Process Tasks

Retrieves tasks for a process in Tallyfy.

```
GET https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-process-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tallyfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-process-tasks?connectionId=$CONNECTION_ID&run_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "run_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-process-tasks?${params}`, {
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
| `run_id` | string | yes | Process ID from Tallyfy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "allow_guest_owners": true,
      "archived_at": "2026-05-07T12:00:00.000Z",
      "blueprint_position": 1,
      "can_complete_only_assignees": true,
      "checklist_id": "string",
      "completed_at": "2026-05-07T12:00:00.000Z",
      "completer_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "deadline": "2026-05-07T12:00:00.000Z",
      "everyone_must_complete": true,
      "has_deadline_dependent_child_tasks": true,
      "id": "string",
      "increment_id": 1,
      "is_approved": true,
      "is_completable": true,
      "is_oneoff_task": true,
      "is_soft_start_date": true,
      "last_updated": "2026-05-07T12:00:00.000Z",
      "linked_step_id": "https://example.com",
      "max_assignable": 1,
      "original_summary": "string",
      "original_title": "string",
      "owners": {
        "groups": [
          [
            "string"
          ]
        ],
        "guests": [
          [
            "string"
          ]
        ],
        "users": [
          [
            1
          ]
        ]
      },
      "position": 1,
      "prevent_guest_comment": true,
      "problem": true,
      "run_id": "string",
      "run_status": "string",
      "send_chromeless": true,
      "stage_id": "string",
      "started_at": "2026-05-07T12:00:00.000Z",
      "starter_id": 1,
      "status": "string",
      "status_label": "string",
      "step_id": "string",
      "summary": "string",
      "task_type": "string",
      "title": "string",
      "top_secret": true,
      "webhook": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `allow_guest_owners` | boolean |  |
| `archived_at` | date |  |
| `blueprint_position` | number |  |
| `can_complete_only_assignees` | boolean |  |
| `checklist_id` | string |  |
| `completed_at` | date |  |
| `completer_id` | number |  |
| `created_at` | date |  |
| `deadline` | date |  |
| `everyone_must_complete` | boolean |  |
| `has_deadline_dependent_child_tasks` | boolean |  |
| `id` | string |  |
| `increment_id` | number |  |
| `is_approved` | boolean |  |
| `is_completable` | boolean |  |
| `is_oneoff_task` | boolean |  |
| `is_soft_start_date` | boolean |  |
| `last_updated` | date |  |
| `linked_step_id` | string |  |
| `max_assignable` | number |  |
| `original_summary` | string |  |
| `original_title` | string |  |
| `owners.groups[]` | array<string> |  |
| `owners.guests[]` | array<string> |  |
| `owners.users[]` | array<number> |  |
| `position` | number |  |
| `prevent_guest_comment` | boolean |  |
| `problem` | boolean |  |
| `run_id` | string |  |
| `run_status` | string |  |
| `send_chromeless` | boolean |  |
| `stage_id` | string |  |
| `started_at` | date |  |
| `starter_id` | number |  |
| `status` | string |  |
| `status_label` | string |  |
| `step_id` | string |  |
| `summary` | string |  |
| `task_type` | string |  |
| `title` | string |  |
| `top_secret` | boolean |  |
| `webhook` | string |  |

## Native endpoint

Through the native Tallyfy API, this operation is `GET /organizations/:org/runs/:run_id/tasks` (base URL `https://api.tallyfy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-tasks.md) for the provider-specific parameters and requirements.

