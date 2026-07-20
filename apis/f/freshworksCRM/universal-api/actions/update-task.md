# Freshworks CRM: Update Task

Updates an existing task in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "task": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "task": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `task` | object | yes |  |
| `task.description` | string | no |  |
| `task.dueDate` | string | no |  |
| `task.ownerId` | number | no |  |
| `task.targetableId` | number | no |  |
| `task.targetableType` | string | no |  |
| `task.title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        [
          {}
        ]
      ],
      "task": {
        "completed_date": "2026-05-07T12:00:00.000Z",
        "created_at": "2026-05-07T12:00:00.000Z",
        "creater_id": 1,
        "description": "string",
        "due_date": "2026-05-07T12:00:00.000Z",
        "has_multiple_emails": true,
        "id": 1,
        "is_linkedin_type": true,
        "outcome_id": 1,
        "owner_id": 1,
        "status": 1,
        "targetable": {
          "id": 1,
          "type": "string"
        },
        "targetables_with_email": [
          [
            {}
          ]
        ],
        "targetables": [
          [
            {}
          ]
        ],
        "task_type_id": 1,
        "title": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "updater_id": 1,
        "user_ids": [
          [
            1
          ]
        ]
      },
      "users": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[]` | array<object> | Related contacts. |
| `contacts[].avatar` | string | Avatar URL. |
| `contacts[].display_name` | string | Display name. |
| `contacts[].email` | string | Email address. |
| `contacts[].first_name` | string | First name. |
| `contacts[].id` | number | Contact identifier. |
| `contacts[].job_title` | string | Job title. |
| `contacts[].last_name` | string | Last name. |
| `contacts[].linkedin` | string | LinkedIn profile. |
| `contacts[].mobile_number` | string | Mobile number. |
| `contacts[].subscription_status` | number | Subscription status. |
| `contacts[].subscription_types` | string | Subscription types. |
| `contacts[].work_number` | string | Work number. |
| `task` | object | Updated task. |
| `task.completed_date` | date | Completed date. |
| `task.created_at` | date | Created timestamp. |
| `task.creater_id` | number | Creator id. |
| `task.description` | string | Task description. |
| `task.due_date` | date | Due date. |
| `task.has_multiple_emails` | boolean | Multiple email flag. |
| `task.id` | number | Task identifier. |
| `task.is_linkedin_type` | boolean | LinkedIn type flag. |
| `task.outcome_id` | number | Outcome id. |
| `task.owner_id` | number | Owner id. |
| `task.status` | number | Task status. |
| `task.targetable.id` | number | Linked target id. |
| `task.targetable.type` | string | Linked target type. |
| `task.targetables_with_email[]` | array<object> | Targeted records with email. |
| `task.targetables_with_email[].id` | number | Targetable id. |
| `task.targetables_with_email[].name` | string | Targetable name. |
| `task.targetables_with_email[].type` | string | Targetable type. |
| `task.targetables[]` | array<object> | Targeted records. |
| `task.targetables[].id` | number | Targetable id. |
| `task.targetables[].type` | string | Targetable type. |
| `task.task_type_id` | number | Task type id. |
| `task.title` | string | Task title. |
| `task.updated_at` | date | Updated timestamp. |
| `task.updater_id` | number | Updater id. |
| `task.user_ids[]` | array<number> | Related user ids. |
| `users[]` | array<object> | Related users. |
| `users[].avatar` | string | Avatar URL. |
| `users[].display_name` | string | Display name. |
| `users[].email` | string | Email address. |
| `users[].id` | number | User identifier. |
| `users[].is_active` | boolean | Active flag. |
| `users[].mobile_number` | string | Mobile number. |
| `users[].type` | string | User type. |
| `users[].uuid` | string | UUID. |
| `users[].work_number` | string | Work number. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `PUT /api/tasks/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

