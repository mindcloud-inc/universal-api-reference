# FreeAgent: Update Project

Updates an existing project in FreeAgent.

```
PUT https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-project', {
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
| `id` | string | yes | FreeAgent project ID. |
| `project` | object | no | Project payload. |
| `project.contact` | string | no | Contact to bill for the project. |
| `project.name` | string | no | Free-text project name. |
| `project.status` | string | no | Project status. |
| `project.currency` | string | no | Project currency code. |
| `project.budget_units` | string | no | Budget units. |
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

Through the native FreeAgent API, this operation is `PUT /projects/:id` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

