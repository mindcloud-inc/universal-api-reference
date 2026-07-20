# Tallyfy Universal API Examples

These examples use the MindCloud API key and Tallyfy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Member

Retrieves the current member from Tallyfy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/get-current-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/get-current-member?${params}`, {
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
      "activated_at": "2026-05-07T12:00:00.000Z",
      "approved_at": "2026-05-07T12:00:00.000Z",
      "cadence_days": [
        "string"
      ],
      "country_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "date_format": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": 1,
      "initial_signup_method": "string",
      "is_active": true,
      "is_default_admin": true,
      "is_partner": true,
      "is_support": true,
      "last_accessed_at": "2026-05-07T12:00:00.000Z",
      "last_city": "string",
      "last_country": "string",
      "last_known_country": "string",
      "last_known_ip": "string",
      "last_login_at": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "phone": "string",
      "profile_pic": "string",
      "resize_profile_pic": "string",
      "role": "string",
      "status": "string",
      "step_preferences": true,
      "timezone": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen",
      "UTC_offset": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Member action reference](actions/get-current-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tallyfy/latest/actions/get-current-member).

## Complete Process Task

Completes a process task in Tallyfy.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/complete-process-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "run_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/complete-process-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "run_id": "string"
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

See the full [Complete Process Task action reference](actions/complete-process-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tallyfy/latest/actions/complete-process-task).
