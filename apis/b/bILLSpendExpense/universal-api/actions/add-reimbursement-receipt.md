# BILL Spend & Expense: Add Reimbursement Receipt

Adds a receipt to a reimbursement in BILL Spend & Expense.

```
POST https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/add-reimbursement-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/add-reimbursement-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "reimbursementId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/add-reimbursement-receipt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "reimbursementId": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | Receipt file name. |
| `reimbursementId` | list | yes | BILL-generated ID or UUID of the reimbursement. |
| `url` | string | yes | Uploaded receipt URL returned by the reimbursement upload URL flow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "url": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `url` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `POST spend/reimbursements/:reimbursementId/receipts` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-reimbursement-receipt.md) for the provider-specific parameters and requirements.

