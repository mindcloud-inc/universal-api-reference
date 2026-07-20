# Campfire: Retrieve Chart Transaction

Retrieves a chart transaction from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-chart-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-chart-transaction?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-chart-transaction?${params}`, {
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
| `id` | number | yes | The chart transaction ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_name": "Ava Chen",
      "account_number": "string",
      "amount": 1,
      "amount_book": 1,
      "amount_native": 1,
      "balance_after_transaction": 1,
      "balance_before_transaction": 1,
      "bank_description": "string",
      "bill_id": 1,
      "bill_number": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "department": 1,
      "department_name": "Ava Chen",
      "entity": 1,
      "entity_currency": "string",
      "entity_name": "Ava Chen",
      "exchange_rate": 1,
      "id": 1,
      "invoice_id": 1,
      "invoice_number": "string",
      "is_deleted": true,
      "journal": 1,
      "journal_memo": "string",
      "journal_order": "string",
      "journal_type": "string",
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "merchant_name": "Ava Chen",
      "needs_review": true,
      "note": "string",
      "posted_at": "2026-05-07T12:00:00.000Z",
      "tags": [
        {}
      ],
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
| `account_name` | string |  |
| `account_number` | string |  |
| `amount` | number |  |
| `amount_book` | number |  |
| `amount_native` | number |  |
| `balance_after_transaction` | number |  |
| `balance_before_transaction` | number |  |
| `bank_description` | string |  |
| `bill_id` | number |  |
| `bill_number` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `department` | number |  |
| `department_name` | string |  |
| `entity` | number |  |
| `entity_currency` | string |  |
| `entity_name` | string |  |
| `exchange_rate` | number |  |
| `id` | number |  |
| `invoice_id` | number |  |
| `invoice_number` | string |  |
| `is_deleted` | boolean |  |
| `journal` | number |  |
| `journal_memo` | string |  |
| `journal_order` | string |  |
| `journal_type` | string |  |
| `last_modified_at` | date |  |
| `merchant_name` | string |  |
| `needs_review` | boolean |  |
| `note` | string |  |
| `posted_at` | date |  |
| `tags` | array<object> |  |
| `vendor` | number |  |
| `vendor_name` | string |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/transaction/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-chart-transaction.md) for the provider-specific parameters and requirements.

