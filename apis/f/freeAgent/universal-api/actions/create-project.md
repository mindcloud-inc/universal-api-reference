# FreeAgent: Create Project

Creates a new project in FreeAgent.

```
POST https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project.contact": "string",
  "project.name": "Ava Chen",
  "project.status": "string",
  "project.currency": "string",
  "project.budget_units": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project.contact": "string",
    "project.name": "Ava Chen",
    "project.status": "string",
    "project.currency": "string",
    "project.budget_units": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | object | no | Project payload. |
| `project.contact` | string | yes | Contact to bill for the project. |
| `project.name` | string | yes | Free-text project name. |
| `project.status` | string | yes | Project status. |
| `project.currency` | string | yes | Project currency code. |
| `project.budget_units` | string | yes | Budget units. |
| `project.budget` | number | no | Project budget. |
| `project.normal_billing_rate` | number | no | Normal billing rate. |
| `project.billing_period` | string | no | Billing period. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_period": "string",
      "budget": 1,
      "budget_units": "string",
      "contact": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "hours_per_day": "string",
      "include_unbilled_time_in_profitability": true,
      "is_deletable": true,
      "name": "Ava Chen",
      "normal_billing_rate": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "uses_project_invoice_sequence": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_period` | string |  |
| `budget` | number |  |
| `budget_units` | string |  |
| `contact` | string |  |
| `contact_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `hours_per_day` | string |  |
| `include_unbilled_time_in_profitability` | boolean |  |
| `is_deletable` | boolean |  |
| `name` | string |  |
| `normal_billing_rate` | string |  |
| `status` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `uses_project_invoice_sequence` | boolean |  |

## Native endpoint

Through the native FreeAgent API, this operation is `POST /projects` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

