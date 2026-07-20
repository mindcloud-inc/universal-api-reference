# Harpoon: List Time Entries

Retrieves time entries from Harpoon.

```
GET https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-time-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-time-entries?${params}`, {
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
| `status` | string | no |  |
| `start` | date | no |  |
| `end` | date | no |  |
| `clients[]` | array<number> | no |  |
| `projects[]` | array<number> | no |  |
| `tasks[]` | array<number> | no |  |
| `profiles[]` | array<number> | no |  |
| `statuses[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billed_status": "string",
      "cost": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hours": 1,
      "id": "string",
      "profile_id": "string",
      "project_id": "string",
      "quantity": 1,
      "seconds": 1,
      "seconds_running": 1,
      "task_id": "string",
      "team_id": "string",
      "timer_status": "string",
      "user_id": "string",
      "value": 1,
      "yield": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billed_status` | string |  |
| `cost` | number |  |
| `date` | date |  |
| `description` | string |  |
| `hours` | number |  |
| `id` | string |  |
| `profile_id` | string |  |
| `project_id` | string |  |
| `quantity` | number |  |
| `seconds` | number |  |
| `seconds_running` | number |  |
| `task_id` | string |  |
| `team_id` | string |  |
| `timer_status` | string |  |
| `user_id` | string |  |
| `value` | number |  |
| `yield` | number |  |

## Native endpoint

Through the native Harpoon API, this operation is `GET /time_entries` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

