# Harpoon: Update Time Entry

Updates an existing time entry in Harpoon.

```
PUT https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `projectId` | number | no |  |
| `taskId` | number | no |  |
| `date` | date | no |  |
| `hours` | number | no |  |
| `description` | string | no |  |
| `billedStatus` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billed_status": "string",
      "cost": 1,
      "date": "string",
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
| `date` | string |  |
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

Through the native Harpoon API, this operation is `PUT /time_entries/:id` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.

