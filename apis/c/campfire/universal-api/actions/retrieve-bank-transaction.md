# Campfire: Retrieve Bank Transaction

Retrieves a bank transaction from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-bank-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-bank-transaction?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-bank-transaction?${params}`, {
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
| `id` | number | yes | The bank transaction ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": 1,
      "account_name": "Ava Chen",
      "amount": 1,
      "amount_native": 1,
      "assigned": true,
      "bank_description": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": 1,
      "date_month": "string",
      "date_year": "string",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "excluded": true,
      "id": 1,
      "is_deleted": true,
      "journal": 1,
      "journal_order": "string",
      "kind": "string",
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "merchant_name": "Ava Chen",
      "note": "string",
      "posted_at": "2026-05-07T12:00:00.000Z",
      "reconciliation_report": 1,
      "reconciliation_report_ending_date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | number |  |
| `account_name` | string |  |
| `amount` | number |  |
| `amount_native` | number |  |
| `assigned` | boolean |  |
| `bank_description` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `customer` | number |  |
| `date_month` | string |  |
| `date_year` | string |  |
| `deleted_at` | date |  |
| `excluded` | boolean |  |
| `id` | number |  |
| `is_deleted` | boolean |  |
| `journal` | number |  |
| `journal_order` | string |  |
| `kind` | string |  |
| `last_modified_at` | date |  |
| `merchant_name` | string |  |
| `note` | string |  |
| `posted_at` | date |  |
| `reconciliation_report` | number |  |
| `reconciliation_report_ending_date` | date |  |
| `status` | string |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /ca/api/transaction/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-bank-transaction.md) for the provider-specific parameters and requirements.

