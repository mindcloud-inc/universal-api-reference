# Harpoon: Update Invoice

Updates an existing invoice in Harpoon.

```
PUT https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-invoice', {
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
| `projectId` | number | no |  |
| `documentId` | string | no |  |
| `issueDate` | date | no |  |
| `dueDate` | date | no |  |
| `status` | string | no |  |
| `discount` | number | no |  |
| `shipping` | number | no |  |
| `lineItems[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accept_ach": true,
      "address": "string",
      "amount_due": 1,
      "amount_paid": 1,
      "auto_billing": true,
      "automatically_send_payment_reminders": true,
      "client_id": 1,
      "company_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "discount": 1,
      "document_id": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "hide_qty_price_columns": true,
      "id": 1,
      "issue_date": "2026-05-07T12:00:00.000Z",
      "note": "string",
      "online_payment": true,
      "outstanding": 1,
      "payment_due": 1,
      "phone": "string",
      "po_number": "string",
      "project_id": 1,
      "send_at": "2026-05-07T12:00:00.000Z",
      "shipping": 1,
      "status": "string",
      "subject": "string",
      "total": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accept_ach` | boolean |  |
| `address` | string |  |
| `amount_due` | number |  |
| `amount_paid` | number |  |
| `auto_billing` | boolean |  |
| `automatically_send_payment_reminders` | boolean |  |
| `client_id` | number |  |
| `company_name` | string |  |
| `created_at` | date |  |
| `discount` | number |  |
| `document_id` | string |  |
| `due_date` | date |  |
| `email` | string |  |
| `hide_qty_price_columns` | boolean |  |
| `id` | number |  |
| `issue_date` | date |  |
| `note` | string |  |
| `online_payment` | boolean |  |
| `outstanding` | number |  |
| `payment_due` | number |  |
| `phone` | string |  |
| `po_number` | string |  |
| `project_id` | number |  |
| `send_at` | date |  |
| `shipping` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `total` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Harpoon API, this operation is `PUT /invoices/:id` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

