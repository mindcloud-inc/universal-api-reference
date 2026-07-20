# Freshworks CRM: Create Task

Creates a new task in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task": {},
  "task.dueDate": "string",
  "task.targetableId": 1,
  "task.targetableType": "string",
  "task.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task": {},
    "task.dueDate": "string",
    "task.targetableId": 1,
    "task.targetableType": "string",
    "task.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task` | object | yes |  |
| `task.description` | string | no |  |
| `task.dueDate` | string | yes | Due date string for the task. Freshworks rejects task creation when due date is blank. |
| `task.ownerId` | number | no |  |
| `task.targetableId` | number | yes |  |
| `task.targetableType` | string | yes |  |
| `task.title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
        "updater_id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `task` | object | Created task. |
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

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/tasks` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

