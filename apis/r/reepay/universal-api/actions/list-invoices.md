# Reepay: List Invoices

Retrieves invoices from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accounting_created_date": "2026-05-07T12:00:00.000Z",
      "accounting_number": "string",
      "amount": 1,
      "amount_ex_vat": 1,
      "amount_vat": 1,
      "cancelled": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": "string",
      "discount_amount": 1,
      "due": "2026-05-07T12:00:00.000Z",
      "handle": "string",
      "id": "string",
      "number": 1,
      "org_amount": 1,
      "plan": "string",
      "processing": true,
      "refunded_amount": 1,
      "settled_amount": 1,
      "state": "string",
      "subscription": "string",
      "transactions": [
        {
          "amount": 1,
          "created": "2026-05-07T12:00:00.000Z",
          "currency": "string",
          "id": "string",
          "invoice": "string",
          "offline_transaction": {
            "offline_mandate": {
              "offline_agreement_handle": "string"
            },
            "offline_payment_instructions": "string",
            "payment_due_date": "2026-05-07T12:00:00.000Z"
          },
          "payment_context": "string",
          "payment_method": "string",
          "payment_type": "string",
          "state": "string",
          "type": "string"
        }
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
| `accounting_created_date` | date |  |
| `accounting_number` | string |  |
| `amount` | number |  |
| `amount_ex_vat` | number |  |
| `amount_vat` | number |  |
| `cancelled` | date |  |
| `created` | date |  |
| `currency` | string |  |
| `customer` | string |  |
| `discount_amount` | number |  |
| `due` | date |  |
| `handle` | string |  |
| `id` | string |  |
| `number` | number |  |
| `org_amount` | number |  |
| `plan` | string |  |
| `processing` | boolean |  |
| `refunded_amount` | number |  |
| `settled_amount` | number |  |
| `state` | string |  |
| `subscription` | string |  |
| `transactions[].amount` | number |  |
| `transactions[].created` | date |  |
| `transactions[].currency` | string |  |
| `transactions[].id` | string |  |
| `transactions[].invoice` | string |  |
| `transactions[].offline_transaction.offline_mandate.offline_agreement_handle` | string |  |
| `transactions[].offline_transaction.offline_payment_instructions` | string |  |
| `transactions[].offline_transaction.payment_due_date` | date |  |
| `transactions[].payment_context` | string |  |
| `transactions[].payment_method` | string |  |
| `transactions[].payment_type` | string |  |
| `transactions[].state` | string |  |
| `transactions[].type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/list/invoice` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

