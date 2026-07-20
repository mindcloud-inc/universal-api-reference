# BILL Spend & Expense: List Budget Members

Retrieves members for a budget in BILL Spend & Expense.

```
GET https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-budget-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-budget-members?connectionId=$CONNECTION_ID&budgetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "budgetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-budget-members?${params}`, {
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
| `max` | number | no | Maximum number of results to return. |
| `nextPage` | string | no | Next page token returned by the previous list response. |
| `prevPage` | string | no | Previous page token returned by the previous list response. |

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
      "recurringLimit": 1,
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
| `recurringLimit` | number |  |
| `retired` | boolean |  |
| `shareBudgetFunds` | boolean |  |
| `spent` | number |  |
| `userId` | string |  |
| `userUuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `GET spend/budgets/:budgetId/members` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-budget-members.md) for the provider-specific parameters and requirements.

