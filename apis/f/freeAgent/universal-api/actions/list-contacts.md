# FreeAgent: List Contacts

Retrieves a list of contacts from FreeAgent.

```
GET https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `view` | string | no | Return all, active, hidden, clients, suppliers, bank accounts, employees, or projects contacts. |
| `updatedSince` | date | no | Only return contacts updated since this ISO 8601 timestamp. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_balance` | string |  |
| `active_projects_count` | number |  |
| `charge_sales_tax` | string |  |
| `contact_name_on_invoices` | boolean |  |
| `country` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `emails_invoices_automatically` | boolean |  |
| `emails_payment_reminders` | boolean |  |
| `emails_thank_you_notes` | boolean |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `locale` | string |  |
| `phone_number` | string |  |
| `status` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `uses_contact_invoice_sequence` | boolean |  |
| `uses_contact_level_email_settings` | boolean |  |

## Native endpoint

Through the native FreeAgent API, this operation is `GET /contacts` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

