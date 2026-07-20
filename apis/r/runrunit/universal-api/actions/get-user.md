# Runrun.it: Get User

Retrieves a user from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | User Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin_runrunit_roles": [
        "string"
      ],
      "alt_id": "string",
      "avatar_large_url": "https://example.com",
      "avatar_url": "https://example.com",
      "birthday": "2026-05-07T12:00:00.000Z",
      "blocked_by_time_worked_at": "2026-05-07T12:00:00.000Z",
      "budget_manager": true,
      "bypass_block_by_time_worked": true,
      "can_create_boards": true,
      "can_create_client_project_and_task_types": true,
      "cost_hour": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "demanders_count": 1,
      "email": "ava@example.com",
      "gender": "string",
      "has_all_users_as_demanders": true,
      "has_all_users_as_partners": true,
      "id": "string",
      "in_company_since": "2026-05-07T12:00:00.000Z",
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
      "legacy_on_vacation": true,
      "marital_status": "string",
      "name": "Ava Chen",
      "oid": "string",
      "on_vacation": true,
      "partners_count": 1,
      "password_expired_at": "2026-05-07T12:00:00.000Z",
      "password_updated_at": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "position": "string",
      "shift_work_time_per_week": 1,
      "shifts": [
        "string"
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
| `admin_runrunit_roles` | array<string> | Runrun.it admin roles (internal use only) |
| `alt_id` | string | Constant size ID (internal use only) |
| `avatar_large_url` | string | User's chosen profile photo |
| `avatar_url` | string | User's chosen profile photo |
| `birthday` | date | User's birthday |
| `blocked_by_time_worked_at` | date | When the user is blocked for being out of the acceptable worked time defined by the company |
| `budget_manager` | boolean | Can edit project extra costs |
| `bypass_block_by_time_worked` | boolean | User ignore the blocking rule for time worked |
| `can_create_boards` | boolean | User has permission to create boards |
| `can_create_client_project_and_task_types` | boolean | User has permission to create client, projects and task types |
| `cost_hour` | number | Current user cost per hour |
| `created_at` | date | User creation date |
| `demanders_count` | number | Demanders count |
| `email` | string | User's email |
| `gender` | string | User gender |
| `has_all_users_as_demanders` | boolean | True if has all users as demanders |
| `has_all_users_as_partners` | boolean | True if user has all users as partners |
| `id` | string | User's ID |
| `in_company_since` | date | Joining date in company |
| `is_auditor` | boolean | User is an auditor |
| `is_blocked_on_mobile` | boolean | User has mobile apps access blocked |
| `is_certified` | boolean | Whether the user has passed RR Starter certification |
| `is_certified_expert` | boolean | Whether the user has passed RR Expert certification |
| `is_eligible_to_access_reports` | boolean | User can access enterprise reports |
| `is_eligible_to_whatsapp` | boolean | User can access whatsapp integration |
| `is_manager` | boolean | User is a manager |
| `is_master` | boolean | User is an administrator |
| `is_mensurable` | boolean | Can process RR Ratings? |
| `language` | string | User preference language |
| `led_team_ids` | array<string> | Ids from teams the user leads |
| `legacy_on_vacation` | boolean | Internal use only |
| `marital_status` | string | User marital status |
| `name` | string | User's full name |
| `oid` | string | Constant size ID (internal use only) |
| `on_vacation` | boolean | User currently on vacation |
| `partners_count` | number | Partners count |
| `password_expired_at` | date | Time when the user password was considered expired |
| `password_updated_at` | date | Last time user password was updated |
| `phone` | string | User phone |
| `position` | string | Job position in company |
| `shift_work_time_per_week` | number | Shift work time (in seconds) per week |
| `shifts` | array<string> | User shifts |
| `skip_time_adjust_on_task_assignment_deliver` | boolean | [Deprecated] Use preferences.skip_time_adjust_on_task_assignment_deliver |
| `task_list_background_image_url` | string | [Deprecated] Use preferences.task_list_background_image_url |
| `team_ids` | array<string> | Ids from teams that the user belongs to |
| `theme` | string | [Deprecated] Use preferences.theme |
| `time_tracking_mode` | string | [Deprecated] Use 'time_tracking_mode' from enterprise |
| `time_zone` | string | IANA Time Zone Database zone name |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /users/:user_id` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

