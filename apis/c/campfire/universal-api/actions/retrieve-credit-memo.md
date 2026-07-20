# Campfire: Retrieve Credit Memo

Retrieves a credit memo from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-credit-memo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-credit-memo?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-credit-memo?${params}`, {
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
| `id` | number | yes | The credit memo ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_remaining": 1,
      "amount_used": 1,
      "application_status": "string",
      "applied_date": "2026-05-07T12:00:00.000Z",
      "attachments": [
        {}
      ],
      "client": 1,
      "client_email": "ava@example.com",
      "client_name": "Ava Chen",
      "contract": 1,
      "contract_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "credit_account": 1,
      "credit_account_name": "Ava Chen",
      "credit_account_number": "string",
      "credit_memo_date": "2026-05-07T12:00:00.000Z",
      "credit_memo_number": "string",
      "currency": "string",
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "entity": 1,
      "entity_currency": "string",
      "entity_name": "Ava Chen",
      "exchange_rate": 1,
      "id": 1,
      "is_deleted": true,
      "journal_entry": 1,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "last_sent_at": "2026-05-07T12:00:00.000Z",
      "lines": [
        {}
      ],
      "message_on_credit_memo": "string",
      "payments": [
        {}
      ],
      "ref_number": "string",
      "total_amount": 1,
      "voided_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_remaining` | number |  |
| `amount_used` | number |  |
| `application_status` | string |  |
| `applied_date` | date |  |
| `attachments` | array<object> |  |
| `client` | number |  |
| `client_email` | string |  |
| `client_name` | string |  |
| `contract` | number |  |
| `contract_name` | string |  |
| `created_at` | date |  |
| `credit_account` | number |  |
| `credit_account_name` | string |  |
| `credit_account_number` | string |  |
| `credit_memo_date` | date |  |
| `credit_memo_number` | string |  |
| `currency` | string |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `entity` | number |  |
| `entity_currency` | string |  |
| `entity_name` | string |  |
| `exchange_rate` | number |  |
| `id` | number |  |
| `is_deleted` | boolean |  |
| `journal_entry` | number |  |
| `last_modified_at` | date |  |
| `last_sent_at` | date |  |
| `lines` | array<object> |  |
| `message_on_credit_memo` | string |  |
| `payments` | array<object> |  |
| `ref_number` | string |  |
| `total_amount` | number |  |
| `voided_date` | date |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/v1/credit-memo/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-credit-memo.md) for the provider-specific parameters and requirements.

