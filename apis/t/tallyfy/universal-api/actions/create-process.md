# Tallyfy: Create Process

Creates a new process from a template in Tallyfy.

```
POST https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/create-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tallyfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/create-process" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/create-process', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_at": "2026-05-07T12:00:00.000Z",
      "can_add_oot": true,
      "checklist_id": "string",
      "checklist_title": "string",
      "completed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "due_date": "2026-05-07T12:00:00.000Z",
      "due_date_passed": true,
      "due_soon": true,
      "id": "string",
      "increment_id": 1,
      "is_public": true,
      "last_updated": "2026-05-07T12:00:00.000Z",
      "late_tasks": 1,
      "max_task_deadline": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner_id": 1,
      "parent_id": "string",
      "prerun_completed_at": "2026-05-07T12:00:00.000Z",
      "prerun_completed_by": 1,
      "prerun_length": 1,
      "prerun_status": "string",
      "progress": {
        "approved": 1,
        "complete": 1,
        "percent": 1,
        "rejected": 1,
        "total": 1
      },
      "starred": true,
      "started_at": "2026-05-07T12:00:00.000Z",
      "started_by": 1,
      "status": "string",
      "summary": "string",
      "type": "string",
      "whole_progress": {
        "approved": 1,
        "complete": 1,
        "percent": 1,
        "rejected": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | date |  |
| `can_add_oot` | boolean |  |
| `checklist_id` | string |  |
| `checklist_title` | string |  |
| `completed_at` | date |  |
| `created_at` | date |  |
| `due_date` | date |  |
| `due_date_passed` | boolean |  |
| `due_soon` | boolean |  |
| `id` | string |  |
| `increment_id` | number |  |
| `is_public` | boolean |  |
| `last_updated` | date |  |
| `late_tasks` | number |  |
| `max_task_deadline` | date |  |
| `name` | string |  |
| `owner_id` | number |  |
| `parent_id` | string |  |
| `prerun_completed_at` | date |  |
| `prerun_completed_by` | number |  |
| `prerun_length` | number |  |
| `prerun_status` | string |  |
| `progress.approved` | number |  |
| `progress.complete` | number |  |
| `progress.percent` | number |  |
| `progress.rejected` | number |  |
| `progress.total` | number |  |
| `starred` | boolean |  |
| `started_at` | date |  |
| `started_by` | number |  |
| `status` | string |  |
| `summary` | string |  |
| `type` | string |  |
| `whole_progress.approved` | number |  |
| `whole_progress.complete` | number |  |
| `whole_progress.percent` | number |  |
| `whole_progress.rejected` | number |  |
| `whole_progress.total` | number |  |

## Native endpoint

Through the native Tallyfy API, this operation is `POST /organizations/:org/runs` (base URL `https://api.tallyfy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-process.md) for the provider-specific parameters and requirements.

