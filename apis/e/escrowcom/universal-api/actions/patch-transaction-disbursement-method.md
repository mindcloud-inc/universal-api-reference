# Escrow.com: Patch Transaction Disbursement Method

Updates a transaction disbursement method in Escrow.com.

```
PUT https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/patch-transaction-disbursement-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/patch-transaction-disbursement-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/patch-transaction-disbursement-method', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionId` | number | yes | The Escrow.com transaction ID. |
| `accountName` | string | no | Name on the account receiving disbursement. |
| `accountType` | string | no | ACH account type, checking or savings. |
| `bankAbaRoutingNumber` | string | no | ABA routing number for ACH disbursement. |
| `bankAccountNumber` | string | no | Bank account number for ACH disbursement. |
| `bankName` | string | no | Name of the bank receiving disbursement. |
| `currency` | string | no | Currency accepted by the disbursement method. |
| `bankAddress` | object | no | Bank address for disbursement. |
| `beneficiaryAddress` | object | no | Beneficiary address for disbursement. |
| `type` | string | no | Disbursement method type, such as ach or wire_transfer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableDisbursementMethods": [
        {}
      ],
      "savedDisbursementMethods": [
        {}
      ],
      "selectedDisbursementMethod": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableDisbursementMethods` | array<object> | Available disbursement methods for the transaction. |
| `savedDisbursementMethods` | array<object> | Saved disbursement method profiles available to use. |
| `selectedDisbursementMethod` | object | Selected disbursement method when one has been chosen. |

## Native endpoint

Through the native Escrow.com API, this operation is `PATCH /transaction/:transaction_id/disbursement_methods` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-transaction-disbursement-method.md) for the provider-specific parameters and requirements.

