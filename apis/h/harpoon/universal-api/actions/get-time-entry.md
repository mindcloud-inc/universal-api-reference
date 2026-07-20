# Harpoon: Get Time Entry

Retrieves a time entry from Harpoon.

```
GET https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/get-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/get-time-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/get-time-entry?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Harpoon API, this operation is `GET /time_entries/:id` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry.md) for the provider-specific parameters and requirements.

