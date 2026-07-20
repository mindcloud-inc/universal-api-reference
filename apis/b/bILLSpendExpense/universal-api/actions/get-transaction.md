# BILL Spend & Expense: Get Transaction

Retrieves a transaction from BILL Spend & Expense.

```
GET https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/get-transaction?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/get-transaction?${params}`, {
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
| `showCustomFieldIds` | string | no | Comma-separated list of custom field IDs or UUIDs to include in the response. |
| `transactionId` | list | yes | BILL-generated ID or UUID of the transaction. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `authorizedTime` | string |  |
| `budgetId` | string |  |
| `budgetName` | string |  |
| `budgetUuid` | string |  |
| `cardId` | string |  |
| `cardLastFour` | string |  |
| `cardPresent` | boolean |  |
| `cardType` | string |  |
| `cardUuid` | string |  |
| `complete` | boolean |  |
| `fees` | number |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `isParent` | boolean |  |
| `isReconciled` | boolean |  |
| `merchantCategoryCode` | string |  |
| `merchantName` | string |  |
| `network` | string |  |
| `occurredTime` | string |  |
| `originalAuthTransactionId` | string |  |
| `originalAuthTransactionUuid` | string |  |
| `rawMerchantName` | string |  |
| `receiptRequired` | boolean |  |
| `receiptStatus` | string |  |
| `receiptSyncStatus` | string |  |
| `reviewRequired` | boolean |  |
| `status` | string |  |
| `transactedAmount` | number |  |
| `transactionType` | string |  |
| `updatedTime` | string |  |
| `userId` | string |  |
| `userName` | string |  |
| `userUuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `GET spend/transactions/:transactionId` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

