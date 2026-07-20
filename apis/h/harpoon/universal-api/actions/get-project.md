# Harpoon: Get Project

Retrieves a project from Harpoon.

```
GET https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/get-project?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual_rate": 1,
      "budget": 1,
      "budget_remaining": 1,
      "budget_reset": "string",
      "budget_used": 1,
      "client": {},
      "client_id": "string",
      "collected": 1,
      "cost": 1,
      "end": "string",
      "end_date": "2026-05-07T12:00:00.000Z",
      "hours": 1,
      "hours_budget": "string",
      "hours_budget_percentage": 1,
      "hours_recorded": "string",
      "id": "string",
      "name": "Ava Chen",
      "profit": 1,
      "start": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "team_id": "string",
      "total_hours_recorded": "string",
      "track_unbilled_fixed_expected_revenue": true,
      "track_unbilled_hours_expected_revenue": true,
      "type": "string",
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
| `actual_rate` | number |  |
| `budget` | number |  |
| `budget_remaining` | number |  |
| `budget_reset` | string |  |
| `budget_used` | number |  |
| `client` | object |  |
| `client_id` | string |  |
| `collected` | number |  |
| `cost` | number |  |
| `end` | string |  |
| `end_date` | date |  |
| `hours` | number |  |
| `hours_budget` | string |  |
| `hours_budget_percentage` | number |  |
| `hours_recorded` | string |  |
| `id` | string |  |
| `name` | string |  |
| `profit` | number |  |
| `start` | string |  |
| `start_date` | date |  |
| `status` | string |  |
| `team_id` | string |  |
| `total_hours_recorded` | string |  |
| `track_unbilled_fixed_expected_revenue` | boolean |  |
| `track_unbilled_hours_expected_revenue` | boolean |  |
| `type` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Harpoon API, this operation is `GET /projects/:id` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

