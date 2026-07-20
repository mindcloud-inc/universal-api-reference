# FreeAgent: Create Contact

Creates a new contact in FreeAgent.

```
POST https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-contact', {
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
| `contact` | object | no | Contact payload. |
| `contact.first_name` | string | no | First name. |
| `contact.last_name` | string | no | Last name. |
| `contact.organisation_name` | string | no | Organisation name. |
| `contact.email` | string | no | Email. |
| `contact.phone_number` | string | no | Telephone. |

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

Through the native FreeAgent API, this operation is `POST /contacts` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

