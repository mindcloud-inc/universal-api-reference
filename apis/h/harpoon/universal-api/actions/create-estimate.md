# Harpoon: Create Estimate

Creates a new estimate in Harpoon.

```
POST https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | no |  |
| `projectId` | number | no |  |
| `documentId` | string | no |  |
| `issueDate` | date | no |  |
| `dueDate` | date | no |  |
| `subject` | string | no |  |
| `note` | string | no |  |
| `lineItems[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accept_ach": 1,
      "address": "string",
      "amount_due": 1,
      "amount_paid": 1,
      "auto_billing": true,
      "automatically_send_payment_reminders": 1,
      "client": {},
      "client_id": 1,
      "company_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "discount": 1,
      "discount_sum": "string",
      "document_id": "string",
      "due_date": "string",
      "email": "ava@example.com",
      "hide_qty_price_columns": 1,
      "id": 1,
      "issue_date": "string",
      "line_item_options": [
        {}
      ],
      "line_items": [
        {}
      ],
      "note": "string",
      "online_payment": 1,
      "outstanding": 1,
      "payment_due": 1,
      "peppol_document_id": "string",
      "peppol_error": "string",
      "peppol_sent_at": "string",
      "peppol_status": "string",
      "peppol_transmission_id": "string",
      "phone": "string",
      "po_number": "string",
      "project": {},
      "project_id": 1,
      "send_at": "string",
      "shipping": 1,
      "status": "string",
      "subject": "string",
      "subtotal": 1,
      "team": {},
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
| `accept_ach` | number |  |
| `address` | string |  |
| `amount_due` | number |  |
| `amount_paid` | number |  |
| `auto_billing` | boolean |  |
| `automatically_send_payment_reminders` | number |  |
| `client` | object |  |
| `client_id` | number |  |
| `company_name` | string |  |
| `created_at` | date |  |
| `discount` | number |  |
| `discount_sum` | string |  |
| `document_id` | string |  |
| `due_date` | string |  |
| `email` | string |  |
| `hide_qty_price_columns` | number |  |
| `id` | number |  |
| `issue_date` | string |  |
| `line_item_options` | array<object> |  |
| `line_items` | array<object> |  |
| `note` | string |  |
| `online_payment` | number |  |
| `outstanding` | number |  |
| `payment_due` | number |  |
| `peppol_document_id` | string |  |
| `peppol_error` | string |  |
| `peppol_sent_at` | string |  |
| `peppol_status` | string |  |
| `peppol_transmission_id` | string |  |
| `phone` | string |  |
| `po_number` | string |  |
| `project` | object |  |
| `project_id` | number |  |
| `send_at` | string |  |
| `shipping` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `subtotal` | number |  |
| `team` | object |  |
| `total` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Harpoon API, this operation is `POST /estimates` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

