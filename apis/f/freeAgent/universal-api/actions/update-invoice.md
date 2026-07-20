# FreeAgent: Update Invoice

Updates an existing invoice in FreeAgent.

```
PUT https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-invoice', {
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
| `id` | string | yes | FreeAgent invoice ID. |
| `invoice` | object | no | Invoice payload. |
| `invoice.contact` | string | no | Contact being invoiced. |
| `invoice.project` | string | no | Project being invoiced. |
| `invoice.reference` | string | no | Invoice reference. |
| `invoice.dated_on` | date | no | Date of invoice in YYYY-MM-DD format. |
| `invoice.due_on` | date | no | When invoice is due, in YYYY-MM-DD format. |
| `invoice.payment_terms_in_days` | number | no | Set to zero to display Due on Receipt on the invoice. |
| `invoice.currency` | string | no | Invoice currency. |
| `invoice.comments` | string | no | Additional text added to the bottom of the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "always_show_bic_and_iban": true,
      "bank_account": "string",
      "comments": "string",
      "contact": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "due_on": "2026-05-07T12:00:00.000Z",
      "due_value": "string",
      "exchange_rate": "string",
      "involves_sales_tax": true,
      "long_status": "string",
      "net_value": "string",
      "omit_header": true,
      "paid_value": "string",
      "payment_terms_in_days": 1,
      "project": "string",
      "reference": "string",
      "send_new_invoice_emails": true,
      "send_reminder_emails": true,
      "send_thank_you_emails": true,
      "show_project_name": true,
      "status": "string",
      "total_value": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `always_show_bic_and_iban` | boolean |  |
| `bank_account` | string |  |
| `comments` | string |  |
| `contact` | string |  |
| `contact_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `dated_on` | date |  |
| `due_on` | date |  |
| `due_value` | string |  |
| `exchange_rate` | string |  |
| `involves_sales_tax` | boolean |  |
| `long_status` | string |  |
| `net_value` | string |  |
| `omit_header` | boolean |  |
| `paid_value` | string |  |
| `payment_terms_in_days` | number |  |
| `project` | string |  |
| `reference` | string |  |
| `send_new_invoice_emails` | boolean |  |
| `send_reminder_emails` | boolean |  |
| `send_thank_you_emails` | boolean |  |
| `show_project_name` | boolean |  |
| `status` | string |  |
| `total_value` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native FreeAgent API, this operation is `PUT /invoices/:id` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

