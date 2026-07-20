# Runrun.it Universal API Examples

These examples use the MindCloud API key and Runrun.it connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Runrun.it.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/runrunit/latest/actions/list-users).

## Add User To Team

Adds a user to a team in Runrun.it.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/add-user-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/add-user-to-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "cost_center": "string",
      "id": 1,
      "leader_id": "string",
      "leader_name": "Ava Chen",
      "master_user_id": "string",
      "master_user_name": "Ava Chen",
      "name": "Ava Chen",
      "user_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add User To Team action reference](actions/add-user-to-team.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/runrunit/latest/actions/add-user-to-team).
