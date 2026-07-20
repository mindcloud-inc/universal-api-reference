# BILL Spend & Expense: Delete Budget Member

Deletes an existing budget member from BILL Spend & Expense.

```
DELETE https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/delete-budget-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/delete-budget-member?connectionId=$CONNECTION_ID&budgetId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "budgetId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/delete-budget-member?${params}`, {
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
| `budgetId` | list | yes | BILL-generated ID or UUID of the budget. |
| `userId` | list | yes | BILL-generated ID or UUID of the user. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BILL Spend & Expense API returns.

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `DELETE spend/budgets/:budgetId/members/:userId` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-budget-member.md) for the provider-specific parameters and requirements.

