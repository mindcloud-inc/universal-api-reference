# Timely: List Tasks

Retrieves tasks from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-tasks?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-tasks?${params}`, {
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
| `accountId` | number | yes | Account ID |
| `projectIds` | string | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `projectIds` | string | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `projectIds` | string | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `projectIds` | string | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | date | no | Filter tasks from this date (inclusive) |
| `upto` | date | no | Filter tasks up to this date (inclusive) |
| `completed` | string | no | Filter by completion status |
| `userIds` | string | no | Comma-separated list of user IDs to filter by |
| `projectIds` | string | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `forecastIds` | string | no | Comma-separated list of task IDs to filter by |
| `sort` | string | no | Field to sort by (default: updated_at) |
| `order` | string | no | Sort order (default: desc) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "completed_at": "string",
      "created_at": "string",
      "description": "string",
      "estimated_duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
      "estimated_minutes": 1,
      "external_id": "string",
      "from": "string",
      "id": 1,
      "label_ids": [
        1
      ],
      "logged_duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
      "manage": true,
      "note": "string",
      "parent_title": "string",
      "planned_duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
      "project": {},
      "title": "string",
      "to": "string",
      "updated_at": "string",
      "user": {},
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean |  |
| `completed_at` | string |  |
| `created_at` | string |  |
| `description` | string |  |
| `estimated_duration` | object |  |
| `estimated_duration.formatted` | string |  |
| `estimated_duration.hours` | number |  |
| `estimated_duration.minutes` | number |  |
| `estimated_duration.seconds` | number |  |
| `estimated_duration.total_hours` | number |  |
| `estimated_duration.total_minutes` | number |  |
| `estimated_duration.total_seconds` | number |  |
| `estimated_minutes` | number |  |
| `external_id` | string |  |
| `from` | string |  |
| `id` | number |  |
| `label_ids` | array<number> |  |
| `logged_duration` | object |  |
| `logged_duration.formatted` | string |  |
| `logged_duration.hours` | number |  |
| `logged_duration.minutes` | number |  |
| `logged_duration.seconds` | number |  |
| `logged_duration.total_hours` | number |  |
| `logged_duration.total_minutes` | number |  |
| `logged_duration.total_seconds` | number |  |
| `manage` | boolean |  |
| `note` | string |  |
| `parent_title` | string |  |
| `planned_duration` | object |  |
| `planned_duration.formatted` | string |  |
| `planned_duration.hours` | number |  |
| `planned_duration.minutes` | number |  |
| `planned_duration.seconds` | number |  |
| `planned_duration.total_hours` | number |  |
| `planned_duration.total_minutes` | number |  |
| `planned_duration.total_seconds` | number |  |
| `project` | object |  |
| `title` | string |  |
| `to` | string |  |
| `updated_at` | string |  |
| `user` | object |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/forecasts` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

