# Billwerkplus: Cancel Invoice

Cancels an invoice in Billwerkplus.

```
PUT https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/cancel-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/cancel-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/cancel-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Invoice id or handle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountExVat": 1,
      "amountVat": 1,
      "cancelled": "string",
      "created": "string",
      "currency": "string",
      "customer": "string",
      "discountAmount": 1,
      "due": "string",
      "handle": "string",
      "id": "string",
      "orderLines": [
        {
          "amount": 1,
          "amountDefinedInclVat": true,
          "amountExVat": 1,
          "amountVat": 1,
          "id": "string",
          "ordertext": "string",
          "origin": "string",
          "quantity": 1,
          "timestamp": "string",
          "unitAmount": 1,
          "unitAmountExVat": 1,
          "unitAmountVat": 1,
          "vat": 1
        }
      ],
      "orgAmount": 1,
      "refundedAmount": 1,
      "settledAmount": 1,
      "state": "string",
      "transactions": [
        {
          "amount": 1,
          "created": "string",
          "currency": "string",
          "id": "string",
          "invoice": "string",
          "offlineTransaction": {
            "offlineMandate": {
              "offlineAgreementHandle": "string",
              "offlineAgreementName": "Ava Chen"
            },
            "offlinePaymentInstructions": "string",
            "paymentDueDate": "string"
          },
          "paymentContext": "string",
          "paymentMethod": "string",
          "paymentType": "string",
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
| `amount` | number |  |
| `amountExVat` | number |  |
| `amountVat` | number |  |
| `cancelled` | string |  |
| `created` | string |  |
| `currency` | string |  |
| `customer` | string |  |
| `discountAmount` | number |  |
| `due` | string |  |
| `handle` | string |  |
| `id` | string |  |
| `orderLines[].amount` | number |  |
| `orderLines[].amountDefinedInclVat` | boolean |  |
| `orderLines[].amountExVat` | number |  |
| `orderLines[].amountVat` | number |  |
| `orderLines[].id` | string |  |
| `orderLines[].ordertext` | string |  |
| `orderLines[].origin` | string |  |
| `orderLines[].quantity` | number |  |
| `orderLines[].timestamp` | string |  |
| `orderLines[].unitAmount` | number |  |
| `orderLines[].unitAmountExVat` | number |  |
| `orderLines[].unitAmountVat` | number |  |
| `orderLines[].vat` | number |  |
| `orgAmount` | number |  |
| `refundedAmount` | number |  |
| `settledAmount` | number |  |
| `state` | string |  |
| `transactions[].amount` | number |  |
| `transactions[].created` | string |  |
| `transactions[].currency` | string |  |
| `transactions[].id` | string |  |
| `transactions[].invoice` | string |  |
| `transactions[].offlineTransaction.offlineMandate.offlineAgreementHandle` | string |  |
| `transactions[].offlineTransaction.offlineMandate.offlineAgreementName` | string |  |
| `transactions[].offlineTransaction.offlinePaymentInstructions` | string |  |
| `transactions[].offlineTransaction.paymentDueDate` | string |  |
| `transactions[].paymentContext` | string |  |
| `transactions[].paymentMethod` | string |  |
| `transactions[].paymentType` | string |  |
| `transactions[].state` | string |  |
| `transactions[].type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Billwerkplus API, this operation is `POST /invoice/:id/cancel` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-invoice.md) for the provider-specific parameters and requirements.

