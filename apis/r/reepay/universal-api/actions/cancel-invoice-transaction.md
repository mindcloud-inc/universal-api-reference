# Reepay: Cancel Invoice Transaction

Cancels an invoice transaction in Reepay.

```
PUT https://connect.mindcloud.co/v1/universal/reepay/latest/actions/cancel-invoice-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/cancel-invoice-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "transaction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reepay/latest/actions/cancel-invoice-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "transaction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Invoice id or handle from Reepay. |
| `transaction` | string | yes | Transaction id from Reepay. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": "string",
      "invoice": "string",
      "offline_transaction": {
        "offline_mandate": {
          "offline_agreement_handle": "string",
          "offline_agreement_name": "Ava Chen"
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created` | date |  |
| `currency` | string |  |
| `id` | string |  |
| `invoice` | string |  |
| `offline_transaction.offline_mandate.offline_agreement_handle` | string |  |
| `offline_transaction.offline_mandate.offline_agreement_name` | string |  |
| `offline_transaction.offline_payment_instructions` | string |  |
| `offline_transaction.payment_due_date` | date |  |
| `payment_context` | string |  |
| `payment_method` | string |  |
| `payment_type` | string |  |
| `state` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `POST /v1/invoice/:id/transaction/:transaction/cancel` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-invoice-transaction.md) for the provider-specific parameters and requirements.

