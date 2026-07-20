# Runrun.it: Create Client

Creates a new client in Runrun.it.

```
POST https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client.name` | string | yes | Client's name |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client.isVisible` | boolean | no | Client is currently visible to be used |
| `client.budgetedHoursMonth` | number | no | Budgeted hours per month |
| `client.budgetedCostMonth` | number | no | Budgeted cost per month |
| `client.customField` | string | no | Custom field |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": 1,
      "activities_0_days_ago": 1,
      "activities_1_days_ago": 1,
      "activities_2_days_ago": 1,
      "activities_3_days_ago": 1,
      "activities_4_days_ago": 1,
      "activities_5_days_ago": 1,
      "activities_6_days_ago": 1,
      "budgeted_cost_month": 1,
      "budgeted_hours_month": 1,
      "cost_pending": 1,
      "cost_total": 1,
      "cost_worked": 1,
      "custom_field": "string",
      "id": 1,
      "is_visible": true,
      "name": "Ava Chen",
      "project_groups": [
        {}
      ],
      "project_ids": [
        "string"
      ],
      "projects_count": 1,
      "time_pending": 1,
      "time_pending_backlog": 1,
      "time_pending_not_assigned": 1,
      "time_pending_queued": 1,
      "time_progress": 1,
      "time_total": 1,
      "time_worked": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | number |  |
| `activities_0_days_ago` | number |  |
| `activities_1_days_ago` | number |  |
| `activities_2_days_ago` | number |  |
| `activities_3_days_ago` | number |  |
| `activities_4_days_ago` | number |  |
| `activities_5_days_ago` | number |  |
| `activities_6_days_ago` | number |  |
| `budgeted_cost_month` | number |  |
| `budgeted_hours_month` | number |  |
| `cost_pending` | number |  |
| `cost_total` | number |  |
| `cost_worked` | number |  |
| `custom_field` | string |  |
| `id` | number |  |
| `is_visible` | boolean |  |
| `name` | string |  |
| `project_groups` | array<object> |  |
| `project_ids` | array<string> |  |
| `projects_count` | number |  |
| `time_pending` | number |  |
| `time_pending_backlog` | number |  |
| `time_pending_not_assigned` | number |  |
| `time_pending_queued` | number |  |
| `time_progress` | number |  |
| `time_total` | number |  |
| `time_worked` | number |  |

## Native endpoint

Through the native Runrun.it API, this operation is `POST /clients` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

