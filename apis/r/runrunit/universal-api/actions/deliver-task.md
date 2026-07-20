# Runrun.it: Deliver Task

Delivers a task in Runrun.it.

```
PUT https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/deliver-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/deliver-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/deliver-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "board_stage_position": "string",
      "client_id": 1,
      "client_name": "Ava Chen",
      "close_date": "string",
      "created_at": "string",
      "current_estimate_seconds": 1,
      "desired_date": "string",
      "desired_date_with_time": "string",
      "desired_start_date": "string",
      "estimate_updated": true,
      "estimated_at": "string",
      "estimated_delivery_date": "string",
      "estimated_start_date": "string",
      "evaluation_status": "string",
      "gantt_bar_end_date": "string",
      "gantt_bar_start_date": "string",
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
      "queue_position": "string",
      "start_date": "string",
      "subtask_parent_position": "string",
      "tags_data": [
        "string"
      ],
      "team_id": "string",
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
| `attachments_count` | number |  |
| `board_id` | number |  |
| `board_name` | string |  |
| `board_stage_description` | string |  |
| `board_stage_id` | number |  |
| `board_stage_name` | string |  |
| `board_stage_position` | string |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `close_date` | string |  |
| `created_at` | string |  |
| `current_estimate_seconds` | number |  |
| `desired_date` | string |  |
| `desired_date_with_time` | string |  |
| `desired_start_date` | string |  |
| `estimate_updated` | boolean |  |
| `estimated_at` | string |  |
| `estimated_delivery_date` | string |  |
| `estimated_start_date` | string |  |
| `evaluation_status` | string |  |
| `gantt_bar_end_date` | string |  |
| `gantt_bar_start_date` | string |  |
| `guest_id` | string |  |
| `guest_name` | string |  |
| `id` | number |  |
| `is_assigned` | boolean |  |
| `is_closed` | boolean |  |
| `is_working_on` | boolean |  |
| `on_going` | boolean |  |
| `project_group_id` | number |  |
| `project_group_is_default` | boolean |  |
| `project_group_name` | string |  |
| `project_id` | number |  |
| `project_name` | string |  |
| `project_sub_group_id` | number |  |
| `project_sub_group_is_default` | boolean |  |
| `project_sub_group_name` | string |  |
| `queue_position` | string |  |
| `start_date` | string |  |
| `subtask_parent_position` | string |  |
| `tags_data` | array<string> |  |
| `team_id` | string |  |
| `team_name` | string |  |
| `title` | string |  |
| `type_color` | string |  |
| `type_id` | number |  |
| `type_name` | string |  |
| `user_id` | string |  |
| `user_name` | string |  |
| `was_reopened` | boolean |  |

## Native endpoint

Through the native Runrun.it API, this operation is `POST /tasks/:id/deliver` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deliver-task.md) for the provider-specific parameters and requirements.

