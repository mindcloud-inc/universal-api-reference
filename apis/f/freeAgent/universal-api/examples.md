# FreeAgent Universal API Examples

These examples use the MindCloud API key and FreeAgent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves a list of contacts from FreeAgent.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "account_balance": "string",
      "active_projects_count": 1,
      "charge_sales_tax": "string",
      "contact_name_on_invoices": true,
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emails_invoices_automatically": true,
      "emails_payment_reminders": true,
      "emails_thank_you_notes": true,
      "first_name": "Ava",
      "last_name": "Chen",
      "locale": "string",
      "phone_number": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "uses_contact_invoice_sequence": true,
      "uses_contact_level_email_settings": true
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freeAgent/latest/actions/list-contacts).

## Create Bill

Creates a new bill in FreeAgent.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bill.contact": "string",
  "bill.reference": "string",
  "bill.dated_on": "2026-05-07T12:00:00.000Z",
  "bill.due_on": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-bill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bill.contact": "string",
    "bill.reference": "string",
    "bill.dated_on": "2026-05-07T12:00:00.000Z",
    "bill.due_on": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "contact": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "due_on": "2026-05-07T12:00:00.000Z",
      "due_value": "string",
      "input_total_values_inc_tax": true,
      "is_locked": true,
      "is_paid_by_hire_purchase": true,
      "long_status": "string",
      "native_due_value": "string",
      "net_value": "string",
      "paid_value": "string",
      "project": "string",
      "reference": "string",
      "status": "string",
      "total_value": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Bill action reference](actions/create-bill.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freeAgent/latest/actions/create-bill).
