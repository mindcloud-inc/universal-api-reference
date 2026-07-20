# Runrun.it: Get Task

Retrieves a task from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments_count": 1,
      "board_id": 1,
      "board_name": "Ava Chen",
      "board_stage_description": "string",
      "board_stage_id": 1,
      "board_stage_name": "Ava Chen",
      "board_stage_position": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "close_date": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "current_estimate_seconds": 1,
      "desired_date": "2026-05-07T12:00:00.000Z",
      "desired_date_with_time": "2026-05-07T12:00:00.000Z",
      "desired_start_date": "2026-05-07T12:00:00.000Z",
      "estimate_updated": true,
      "estimated_at": true,
      "estimated_delivery_date": "2026-05-07T12:00:00.000Z",
      "estimated_start_date": "2026-05-07T12:00:00.000Z",
      "evaluation_status": "string",
      "gantt_bar_end_date": "2026-05-07T12:00:00.000Z",
      "gantt_bar_start_date": "2026-05-07T12:00:00.000Z",
      "guest_id": "string",
      "guest_name": "Ava Chen",
      "id": 1,
      "is_assigned": true,
      "is_closed": true,
      "is_working_on": true,
      "on_going": true,
      "project_group_id": 1,
      "project_group_is_default": true,
      "project_group_name": "Ava Chen",
      "project_id": 1,
      "project_name": "Ava Chen",
      "project_sub_group_id": 1,
      "project_sub_group_is_default": true,
      "project_sub_group_name": "Ava Chen",
      "queue_position": 1,
      "start_date": "2026-05-07T12:00:00.000Z",
      "subtask_parent_position": 1,
      "tags_data": [
        "string"
      ],
      "team_id": 1,
      "team_name": "Ava Chen",
      "title": "string",
      "type_color": "string",
      "type_id": 1,
      "type_name": "Ava Chen",
      "user_id": "string",
      "user_name": "Ava Chen",
      "was_reopened": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments_count` | number | Number of attachment that belongs to task |
| `board_id` | number | ID of the board the task belongs to |
| `board_name` | string | Name of board |
| `board_stage_description` | string | Description of board stage |
| `board_stage_id` | number | ID of the board stage the task belongs to |
| `board_stage_name` | string | Name of board stage |
| `board_stage_position` | number | Position of the task on stage |
| `client_id` | number | ID of the client the task belongs to |
| `client_name` | string | Name of client |
| `close_date` | date | Date when the task was delivered |
| `created_at` | date | Date when task was created |
| `current_estimate_seconds` | number | Current estimated effort (in seconds) |
| `desired_date` | date | Desired delivery date |
| `desired_date_with_time` | date | Desired delivery date and time |
| `desired_start_date` | date | Desired start date |
| `estimate_updated` | boolean | True if estimate dates have been updated after potential change |
| `estimated_at` | boolean | Last time when task was estimated |
| `estimated_delivery_date` | date | Date when the system estimates the task will be delivered |
| `estimated_start_date` | date | Date when the system estimates the task will be started |
| `evaluation_status` | string | Evaluation status ('approved' / 'rejected' / 'pending' / null) |
| `gantt_bar_end_date` | date | End date for Gantt chart |
| `gantt_bar_start_date` | date | Start date for Gantt chart |
| `guest_id` | string | ID of guest user who created the task |
| `guest_name` | string | Name of guest user who created the task |
| `id` | number | Task ID |
| `is_assigned` | boolean | True if the task has anyone assigned |
| `is_closed` | boolean | True if the task is delivered |
| `is_working_on` | boolean | True if any assignee is working on task |
| `on_going` | boolean | True if the task is an ongoing task |
| `project_group_id` | number | ID of the group the task belongs to |
| `project_group_is_default` | boolean | True if the project group is default |
| `project_group_name` | string | Name of project group |
| `project_id` | number | ID of the project the task belongs to |
| `project_name` | string | Name of project |
| `project_sub_group_id` | number | ID of the sub group the task belongs to |
| `project_sub_group_is_default` | boolean | True if the project subgroup is default |
| `project_sub_group_name` | string | Name of project subgroup |
| `queue_position` | number | 1-based index of position on assignee user's task list |
| `start_date` | date | First time when task was worked on |
| `subtask_parent_position` | number | Position of the task on parent task |
| `tags_data` | array<string> | Tags for task |
| `team_id` | number | ID of the team the task belongs to (if not assigned) |
| `team_name` | string | Name of team (if not assigned) |
| `title` | string | Task title |
| `type_color` | string | Task type color in hexadecimal format |
| `type_id` | number | ID of the task type |
| `type_name` | string | Name of task type |
| `user_id` | string | ID of user who created the task |
| `user_name` | string | Name of user who created the task |
| `was_reopened` | boolean | True if the task has been reopened after being delivered |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /tasks/:id` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

