# FreeAgent: Get Project

Retrieves detailed project information from FreeAgent.

```
GET https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | FreeAgent project ID. |

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

Through the native FreeAgent API, this operation is `GET /projects/:id` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

