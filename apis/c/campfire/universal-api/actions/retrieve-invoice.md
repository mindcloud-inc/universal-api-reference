# Campfire: Retrieve Invoice

Retrieves an invoice from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-invoice?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-invoice?${params}`, {
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
| `id` | number | yes | The invoice ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_due": 1,
      "amount_paid": 1,
      "ar_account": 1,
      "attachments": [
        {}
      ],
      "auto_sent_at": "2026-05-07T12:00:00.000Z",
      "client": 1,
      "client_email": "ava@example.com",
      "client_name": "Ava Chen",
      "contract": 1,
      "contract_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "discount": 1,
      "due_date": "2026-05-07T12:00:00.000Z",
      "emails": [
        {}
      ],
      "entity": 1,
      "entity_currency": "string",
      "entity_name": "Ava Chen",
      "exchange_rate": 1,
      "id": 1,
      "invoice_date": "2026-05-07T12:00:00.000Z",
      "invoice_number": "string",
      "is_deleted": true,
      "item_date": "2026-05-07T12:00:00.000Z",
      "journal_entry": 1,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "last_sent_at": "2026-05-07T12:00:00.000Z",
      "lines": [
        {}
      ],
      "paid_date": "2026-05-07T12:00:00.000Z",
      "past_due_days": 1,
      "payment_journal_entries": [
        1
      ],
      "payment_term": 1,
      "payment_term_name": "Ava Chen",
      "payments": [
        {}
      ],
      "ref_number": "string",
      "related_journal_entries": [
        {}
      ],
      "sent_date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "total_amount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_due` | number |  |
| `amount_paid` | number |  |
| `ar_account` | number |  |
| `attachments` | array<object> |  |
| `auto_sent_at` | date |  |
| `client` | number |  |
| `client_email` | string |  |
| `client_name` | string |  |
| `contract` | number |  |
| `contract_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `discount` | number |  |
| `due_date` | date |  |
| `emails` | array<object> |  |
| `entity` | number |  |
| `entity_currency` | string |  |
| `entity_name` | string |  |
| `exchange_rate` | number |  |
| `id` | number |  |
| `invoice_date` | date |  |
| `invoice_number` | string |  |
| `is_deleted` | boolean |  |
| `item_date` | date |  |
| `journal_entry` | number |  |
| `last_modified_at` | date |  |
| `last_sent_at` | date |  |
| `lines` | array<object> |  |
| `paid_date` | date |  |
| `past_due_days` | number |  |
| `payment_journal_entries` | array<number> |  |
| `payment_term` | number |  |
| `payment_term_name` | string |  |
| `payments` | array<object> |  |
| `ref_number` | string |  |
| `related_journal_entries` | array<object> |  |
| `sent_date` | date |  |
| `status` | string |  |
| `total_amount` | number |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/v1/invoice/:id/` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-invoice.md) for the provider-specific parameters and requirements.

