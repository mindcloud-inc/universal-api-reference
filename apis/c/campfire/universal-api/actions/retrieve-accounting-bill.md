# Campfire: Retrieve Accounting Bill

Retrieves an accounting bill from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-accounting-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-accounting-bill?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-accounting-bill?${params}`, {
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
| `id` | number | yes | The accounting bill ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_due": 1,
      "amount_paid": 1,
      "ap_account": 1,
      "ap_account_name": "Ava Chen",
      "attachments": [
        {}
      ],
      "bill_date": "2026-05-07T12:00:00.000Z",
      "bill_number": "string",
      "bill_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "due_date": "2026-05-07T12:00:00.000Z",
      "entity": 1,
      "entity_currency": "string",
      "entity_name": "Ava Chen",
      "exchange_rate": 1,
      "id": 1,
      "is_deleted": true,
      "journal_entry": 1,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "lines": [
        {}
      ],
      "message_on_bill": "string",
      "paid_date": "2026-05-07T12:00:00.000Z",
      "past_due_days": 1,
      "payment_journal_entries": [
        1
      ],
      "payment_status": "string",
      "payment_term": 1,
      "payment_term_name": "Ava Chen",
      "payments": [
        {}
      ],
      "status": "string",
      "total_amount": 1,
      "vendor": 1,
      "vendor_name": "Ava Chen"
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
| `ap_account` | number |  |
| `ap_account_name` | string |  |
| `attachments` | array<object> |  |
| `bill_date` | date |  |
| `bill_number` | string |  |
| `bill_type` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `due_date` | date |  |
| `entity` | number |  |
| `entity_currency` | string |  |
| `entity_name` | string |  |
| `exchange_rate` | number |  |
| `id` | number |  |
| `is_deleted` | boolean |  |
| `journal_entry` | number |  |
| `last_modified_at` | date |  |
| `lines` | array<object> |  |
| `message_on_bill` | string |  |
| `paid_date` | date |  |
| `past_due_days` | number |  |
| `payment_journal_entries` | array<number> |  |
| `payment_status` | string |  |
| `payment_term` | number |  |
| `payment_term_name` | string |  |
| `payments` | array<object> |  |
| `status` | string |  |
| `total_amount` | number |  |
| `vendor` | number |  |
| `vendor_name` | string |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/v1/bill/:id/` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-accounting-bill.md) for the provider-specific parameters and requirements.

