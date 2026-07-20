# Runrun.it: List Project Users

Retrieves users related to a project in Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-project-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-project-users?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-project-users?${params}`, {
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
      "alt_id": "string",
      "avatar_large_url": "https://example.com",
      "avatar_url": "https://example.com",
      "birthday": "string",
      "blocked_by_time_worked_at": "string",
      "budget_manager": true,
      "bypass_block_by_time_worked": true,
      "can_create_boards": true,
      "can_create_client_project_and_task_types": true,
      "cost_hour": 1,
      "created_at": "string",
      "demanders_count": 1,
      "email": "ava@example.com",
      "gender": "string",
      "has_all_users_as_demanders": true,
      "has_all_users_as_partners": true,
      "id": "string",
      "in_company_since": "string",
      "is_auditor": true,
      "is_blocked_on_mobile": true,
      "is_certified": true,
      "is_certified_expert": true,
      "is_eligible_to_access_reports": true,
      "is_eligible_to_whatsapp": true,
      "is_manager": true,
      "is_master": true,
      "is_mensurable": true,
      "language": "string",
      "led_team_ids": [
        "string"
      ],
      "marital_status": "string",
      "name": "Ava Chen",
      "oid": "string",
      "on_vacation": true,
      "partners_count": 1,
      "password_expired_at": "string",
      "password_updated_at": "string",
      "phone": "string",
      "position": "string",
      "preferences": {
        "skip_time_adjust_on_task_assignment_deliver": true,
        "task_list_background_image_url": "https://example.com",
        "theme": "string"
      },
      "shift_work_time_per_week": 1,
      "shifts": [
        {}
      ],
      "skip_time_adjust_on_task_assignment_deliver": true,
      "task_list_background_image_url": "https://example.com",
      "team_ids": [
        "string"
      ],
      "theme": "string",
      "time_tracking_mode": "string",
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt_id` | string |  |
| `avatar_large_url` | string |  |
| `avatar_url` | string |  |
| `birthday` | string |  |
| `blocked_by_time_worked_at` | string |  |
| `budget_manager` | boolean |  |
| `bypass_block_by_time_worked` | boolean |  |
| `can_create_boards` | boolean |  |
| `can_create_client_project_and_task_types` | boolean |  |
| `cost_hour` | number |  |
| `created_at` | string |  |
| `demanders_count` | number |  |
| `email` | string |  |
| `gender` | string |  |
| `has_all_users_as_demanders` | boolean |  |
| `has_all_users_as_partners` | boolean |  |
| `id` | string |  |
| `in_company_since` | string |  |
| `is_auditor` | boolean |  |
| `is_blocked_on_mobile` | boolean |  |
| `is_certified` | boolean |  |
| `is_certified_expert` | boolean |  |
| `is_eligible_to_access_reports` | boolean |  |
| `is_eligible_to_whatsapp` | boolean |  |
| `is_manager` | boolean |  |
| `is_master` | boolean |  |
| `is_mensurable` | boolean |  |
| `language` | string |  |
| `led_team_ids` | array<string> |  |
| `marital_status` | string |  |
| `name` | string |  |
| `oid` | string |  |
| `on_vacation` | boolean |  |
| `partners_count` | number |  |
| `password_expired_at` | string |  |
| `password_updated_at` | string |  |
| `phone` | string |  |
| `position` | string |  |
| `preferences` | object |  |
| `preferences.skip_time_adjust_on_task_assignment_deliver` | boolean |  |
| `preferences.task_list_background_image_url` | string |  |
| `preferences.theme` | string |  |
| `shift_work_time_per_week` | number |  |
| `shifts` | array<object> |  |
| `skip_time_adjust_on_task_assignment_deliver` | boolean |  |
| `task_list_background_image_url` | string |  |
| `team_ids` | array<string> |  |
| `theme` | string |  |
| `time_tracking_mode` | string |  |
| `time_zone` | string |  |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /projects/:id/related_users` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-users.md) for the provider-specific parameters and requirements.

