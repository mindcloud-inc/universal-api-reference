# FreeAgent: Update Expense

Updates an existing expense in FreeAgent.

```
PUT https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-expense', {
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
| `id` | string | yes | FreeAgent expense ID. |
| `expense` | object | no | Expense payload. |
| `expense.user` | string | no | Expense claimant. |
| `expense.category` | string | no | Expense category. |
| `expense.dated_on` | date | no | Date of expense in YYYY-MM-DD format. |
| `expense.description` | string | no | Free-text description. |
| `expense.gross_value` | number | no | Total value expressed in the given currency. |
| `expense.currency` | string | no | Expense currency. |
| `expense.sales_tax_status` | string | no | Sales tax status. |
| `expense.project` | string | no | Project to rebill. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "gross_value": "string",
      "native_gross_value": "string",
      "project": "string",
      "project_name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `contact_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `dated_on` | date |  |
| `description` | string |  |
| `gross_value` | string |  |
| `native_gross_value` | string |  |
| `project` | string |  |
| `project_name` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user` | string |  |

## Native endpoint

Through the native FreeAgent API, this operation is `PUT /expenses/:id` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-expense.md) for the provider-specific parameters and requirements.

