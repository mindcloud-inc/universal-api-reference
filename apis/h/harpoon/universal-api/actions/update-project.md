# Harpoon: Update Project

Updates an existing project in Harpoon.

```
PUT https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `clientId` | number | no |  |
| `projectName` | string | no |  |
| `type` | string | no |  |
| `projectStatus` | string | no |  |
| `projectStart` | date | no |  |
| `projectEnd` | date | no |  |
| `budget` | number | no |  |
| `budgetReset` | string | no |  |
| `trackUnbilledHoursExpectedRevenue` | boolean | no |  |
| `customTaskRates` | object | no |  |

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
      "end_date": "string",
      "hours": 1,
      "hours_budget": "string",
      "hours_budget_percentage": 1,
      "hours_recorded": "string",
      "id": "string",
      "name": "Ava Chen",
      "profit": 1,
      "start": "string",
      "start_date": "string",
      "status": "string",
      "team_id": "string",
      "total_hours_recorded": 1,
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
| `end_date` | string |  |
| `hours` | number |  |
| `hours_budget` | string |  |
| `hours_budget_percentage` | number |  |
| `hours_recorded` | string |  |
| `id` | string |  |
| `name` | string |  |
| `profit` | number |  |
| `start` | string |  |
| `start_date` | string |  |
| `status` | string |  |
| `team_id` | string |  |
| `total_hours_recorded` | number |  |
| `track_unbilled_fixed_expected_revenue` | boolean |  |
| `track_unbilled_hours_expected_revenue` | boolean |  |
| `type` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Harpoon API, this operation is `PUT /projects/:id` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

