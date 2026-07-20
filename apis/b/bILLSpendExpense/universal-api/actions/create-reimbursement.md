# BILL Spend & Expense: Create Reimbursement

Creates a new reimbursement in BILL Spend & Expense.

```
POST https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-reimbursement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-reimbursement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "budgetId": "string",
  "merchantName": "Ava Chen",
  "note": "string",
  "occurredDate": "yyyy-MM-dd",
  "userId": "string",
  "receiptUrl": "https://example.com",
  "receiptFilename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-reimbursement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "budgetId": "string",
    "merchantName": "Ava Chen",
    "note": "string",
    "occurredDate": "yyyy-MM-dd",
    "userId": "string",
    "receiptUrl": "https://example.com",
    "receiptFilename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Reimbursement amount. |
| `budgetId` | list | yes | BILL-generated ID of the budget used for the reimbursement. |
| `customFields[]` | array<object> | no | Custom field objects and values for the reimbursement. |
| `merchantName` | string | yes | Merchant name for the expense. |
| `note` | string | yes | Business purpose for the expense. |
| `occurredDate` | string | yes | Expense date in yyyy-MM-dd format, for example 2026-10-15. Example: `yyyy-MM-dd`. |
| `userId` | list | yes | BILL-generated ID of the user to be reimbursed. |
| `receiptUrl` | string | yes | Use the upload URL returned by Create Reimbursement Upload URL after uploading the JPG or PNG receipt image to that URL. |
| `receiptFilename` | string | yes | Receipt file name with extension, for example receipt.jpg or receipt.png. BILL stores this together with the uploaded receipt URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "budgetId": "string",
      "budgetUuid": "string",
      "fundRequestAmount": 1,
      "fundRequestBudgetAmount": 1,
      "id": "string",
      "merchantName": "Ava Chen",
      "note": "string",
      "occurredDate": "string",
      "receipts": [
        {
          "filename": "Ava Chen",
          "url": "https://example.com",
          "uuid": "string"
        }
      ],
      "retired": true,
      "status": "string",
      "statusHistory": [
        {
          "actorId": "string",
          "actorRole": "string",
          "note": "string",
          "occurredTime": "string",
          "status": "string"
        }
      ],
      "submittedTime": "string",
      "type": "string",
      "userId": "string",
      "userUuid": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `budgetId` | string |  |
| `budgetUuid` | string |  |
| `fundRequestAmount` | number |  |
| `fundRequestBudgetAmount` | number |  |
| `id` | string |  |
| `merchantName` | string |  |
| `note` | string |  |
| `occurredDate` | string |  |
| `receipts[].filename` | string |  |
| `receipts[].url` | string |  |
| `receipts[].uuid` | string |  |
| `retired` | boolean |  |
| `status` | string |  |
| `statusHistory[].actorId` | string |  |
| `statusHistory[].actorRole` | string |  |
| `statusHistory[].note` | string |  |
| `statusHistory[].occurredTime` | string |  |
| `statusHistory[].status` | string |  |
| `submittedTime` | string |  |
| `type` | string |  |
| `userId` | string |  |
| `userUuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `POST spend/reimbursements` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reimbursement.md) for the provider-specific parameters and requirements.

