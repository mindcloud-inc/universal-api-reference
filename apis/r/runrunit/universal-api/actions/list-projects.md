# Runrun.it: List Projects

Retrieves projects from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-projects?${params}`, {
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
      "activities_3_days_ago": 1,
      "activities_4_days_ago": 1,
      "activities_5_days_ago": 1,
      "activities_6_days_ago": 1,
      "board_stage_id": "string",
      "budgeted_cost": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "close_date": "string",
      "cost_pending": 1,
      "cost_progress": "string",
      "cost_total": 1,
      "cost_worked": 1,
      "created_at": "string",
      "desired_date": "string",
      "extra_costs": 1,
      "id": 1,
      "is_closed": true,
      "is_public": true,
      "is_shared": true,
      "name": "Ava Chen",
      "over_budget": "string",
      "overdue": "string",
      "project_group_id": 1,
      "project_group_is_default": true,
      "project_group_name": "Ava Chen",
      "project_sub_group_id": 1,
      "project_sub_group_is_default": true,
      "project_sub_group_name": "Ava Chen",
      "sharing_details": [
        "string"
      ],
      "start_date": "string",
      "task_points_closed_sum": 1,
      "task_points_not_assigned_sum": 1,
      "task_points_progress": "string",
      "task_points_queued_sum": 1,
      "task_points_sum": 1,
      "task_points_working_on_sum": 1,
      "tasks_closed_count": 1,
      "tasks_count": 1,
      "tasks_count_progress": 1,
      "tasks_not_assigned_count": 1,
      "tasks_queued_count": 1,
      "tasks_working_on_count": 1,
      "time_pending": 1,
      "time_pending_not_assigned": 1,
      "time_pending_queued": 1,
      "time_progress": 1,
      "time_total": 1,
      "time_worked": 1,
      "use_new_permissions": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities_3_days_ago` | number |  |
| `activities_4_days_ago` | number |  |
| `activities_5_days_ago` | number |  |
| `activities_6_days_ago` | number |  |
| `board_stage_id` | string |  |
| `budgeted_cost` | number |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `close_date` | string |  |
| `cost_pending` | number |  |
| `cost_progress` | string |  |
| `cost_total` | number |  |
| `cost_worked` | number |  |
| `created_at` | string |  |
| `desired_date` | string |  |
| `extra_costs` | number |  |
| `id` | number |  |
| `is_closed` | boolean |  |
| `is_public` | boolean |  |
| `is_shared` | boolean |  |
| `name` | string |  |
| `over_budget` | string |  |
| `overdue` | string |  |
| `project_group_id` | number |  |
| `project_group_is_default` | boolean |  |
| `project_group_name` | string |  |
| `project_sub_group_id` | number |  |
| `project_sub_group_is_default` | boolean |  |
| `project_sub_group_name` | string |  |
| `sharing_details` | array<string> |  |
| `start_date` | string |  |
| `task_points_closed_sum` | number |  |
| `task_points_not_assigned_sum` | number |  |
| `task_points_progress` | string |  |
| `task_points_queued_sum` | number |  |
| `task_points_sum` | number |  |
| `task_points_working_on_sum` | number |  |
| `tasks_closed_count` | number |  |
| `tasks_count` | number |  |
| `tasks_count_progress` | number |  |
| `tasks_not_assigned_count` | number |  |
| `tasks_queued_count` | number |  |
| `tasks_working_on_count` | number |  |
| `time_pending` | number |  |
| `time_pending_not_assigned` | number |  |
| `time_pending_queued` | number |  |
| `time_progress` | number |  |
| `time_total` | number |  |
| `time_worked` | number |  |
| `use_new_permissions` | boolean |  |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /projects` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

