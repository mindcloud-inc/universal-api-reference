# BILL Spend & Expense: Add or Update Budget Member

Adds or updates a budget member in BILL Spend & Expense.

```
PUT https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/upsert-budget-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/upsert-budget-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "budgetId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/upsert-budget-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "budgetId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `budgetId` | list | yes | BILL-generated ID or UUID of the budget. |
| `limit` | number | no | Funds assigned to the user in the current budget period. |
| `recurringLimit` | number | no | Funds assigned to the user in future budget periods. |
| `role` | string | no | Budget user role. |
| `shareBudgetFunds` | boolean | no | Set true to share all budget funds with the user. |
| `userId` | list | yes | BILL-generated ID or UUID of the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "budgetRole": "string",
      "limit": 1,
      "name": "Ava Chen",
      "recurring": true,
      "retired": true,
      "shareBudgetFunds": true,
      "spent": 1,
      "userId": "string",
      "userUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budgetRole` | string |  |
| `limit` | number |  |
| `name` | string |  |
| `recurring` | boolean |  |
| `retired` | boolean |  |
| `shareBudgetFunds` | boolean |  |
| `spent` | number |  |
| `userId` | string |  |
| `userUuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `PUT spend/budgets/:budgetId/members/:userId` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-budget-member.md) for the provider-specific parameters and requirements.

