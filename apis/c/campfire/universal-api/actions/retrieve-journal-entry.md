# Campfire: Retrieve Journal Entry

Retrieves a journal entry from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-journal-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-journal-entry?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-journal-entry?${params}`, {
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
| `id` | number | yes | The journal entry ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "bulk_upload": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "credit_memos": [
        {}
      ],
      "currency": "string",
      "customer": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "debit_memos": [
        {}
      ],
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "entity": 1,
      "entity_currency": "string",
      "entity_name": "Ava Chen",
      "exchange_rate": 1,
      "id": 1,
      "invoice": 1,
      "is_deleted": true,
      "journal_id": "string",
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "memo": "string",
      "order": "string",
      "ref_number": "string",
      "revenue_transactions": [
        1
      ],
      "reversal_date": "2026-05-07T12:00:00.000Z",
      "reversal_of_order": "string",
      "reversals": [
        {}
      ],
      "source": "string",
      "source_id": "string",
      "transactions": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `bulk_upload` | boolean |  |
| `created_at` | date |  |
| `credit_memos` | array<object> |  |
| `currency` | string |  |
| `customer` | number |  |
| `date` | date |  |
| `debit_memos` | array<object> |  |
| `deleted_at` | date |  |
| `entity` | number |  |
| `entity_currency` | string |  |
| `entity_name` | string |  |
| `exchange_rate` | number |  |
| `id` | number |  |
| `invoice` | number |  |
| `is_deleted` | boolean |  |
| `journal_id` | string |  |
| `last_modified_at` | date |  |
| `memo` | string |  |
| `order` | string |  |
| `ref_number` | string |  |
| `revenue_transactions` | array<number> |  |
| `reversal_date` | date |  |
| `reversal_of_order` | string |  |
| `reversals` | array<object> |  |
| `source` | string |  |
| `source_id` | string |  |
| `transactions` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/journal_entry/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-journal-entry.md) for the provider-specific parameters and requirements.

