# BILL Spend & Expense Universal API Examples

These examples use the MindCloud API key and BILL Spend & Expense connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Transactions

Retrieves transactions from BILL Spend & Expense.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-transactions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "authorizedTime": "string",
      "budgetId": "string",
      "budgetName": "Ava Chen",
      "budgetUuid": "string",
      "cardId": "string",
      "cardLastFour": "string",
      "cardPresent": true,
      "cardType": "string",
      "cardUuid": "string",
      "complete": true,
      "fees": 1,
      "id": "string",
      "isLocked": true,
      "isParent": true,
      "isReconciled": true,
      "merchantCategoryCode": "string",
      "merchantName": "Ava Chen",
      "network": "string",
      "occurredTime": "string",
      "originalAuthTransactionId": "string",
      "originalAuthTransactionUuid": "string",
      "rawMerchantName": "Ava Chen",
      "receiptRequired": true,
      "receiptStatus": "string",
      "receiptSyncStatus": "string",
      "reviewRequired": true,
      "status": "string",
      "transactedAmount": 1,
      "transactionType": "string",
      "updatedTime": "string",
      "userId": "string",
      "userName": "Ava Chen",
      "userUuid": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Transactions action reference](actions/list-transactions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bILLSpendExpense/latest/actions/list-transactions).

## Add Reimbursement Receipt

Adds a receipt to a reimbursement in BILL Spend & Expense.

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

Example response:

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

See the full [Add Reimbursement Receipt action reference](actions/add-reimbursement-receipt.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bILLSpendExpense/latest/actions/add-reimbursement-receipt).
