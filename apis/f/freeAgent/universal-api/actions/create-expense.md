# FreeAgent: Create Expense

Creates a new expense in FreeAgent.

```
POST https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "expense.user": "string",
  "expense.category": "string",
  "expense.dated_on": "2026-05-07T12:00:00.000Z",
  "expense.description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "expense.user": "string",
    "expense.category": "string",
    "expense.dated_on": "2026-05-07T12:00:00.000Z",
    "expense.description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expense` | object | no | Expense payload. |
| `expense.user` | string | yes | Expense claimant. |
| `expense.category` | string | yes | Expense category. |
| `expense.dated_on` | date | yes | Date of expense in YYYY-MM-DD format. |
| `expense.description` | string | yes | Free-text description. |
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

Through the native FreeAgent API, this operation is `POST /expenses` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

