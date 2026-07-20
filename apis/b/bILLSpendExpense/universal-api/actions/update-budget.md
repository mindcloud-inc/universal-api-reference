# BILL Spend & Expense: Update Budget

Updates an existing budget in BILL Spend & Expense.

```
PUT https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/update-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/update-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "budgetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/update-budget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "budgetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `budgetId` | list | yes | BILL-generated ID or UUID of the budget. |
| `description` | string | no | Budget description. |
| `limit` | string | no | Budget spend limit for the current period. |
| `name` | string | no | Budget name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoAddUsers": true,
      "budgetGroup": true,
      "carryOver": true,
      "currentPeriod": {
        "assigned": 1,
        "limit": 1,
        "spent": {
          "cleared": 1,
          "pending": 1,
          "total": 1
        },
        "startDate": "string"
      },
      "default": true,
      "description": "string",
      "id": "string",
      "limitlessOverspend": true,
      "name": "Ava Chen",
      "receiptRequired": true,
      "recurringInterval": "string",
      "recurringLimit": 1,
      "retired": true,
      "shareFunds": "string",
      "startDate": "string",
      "timezone": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoAddUsers` | boolean |  |
| `budgetGroup` | boolean |  |
| `carryOver` | boolean |  |
| `currentPeriod.assigned` | number |  |
| `currentPeriod.limit` | number |  |
| `currentPeriod.spent.cleared` | number |  |
| `currentPeriod.spent.pending` | number |  |
| `currentPeriod.spent.total` | number |  |
| `currentPeriod.startDate` | string |  |
| `default` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `limitlessOverspend` | boolean |  |
| `name` | string |  |
| `receiptRequired` | boolean |  |
| `recurringInterval` | string |  |
| `recurringLimit` | number |  |
| `retired` | boolean |  |
| `shareFunds` | string |  |
| `startDate` | string |  |
| `timezone` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `PATCH spend/budgets/:budgetId` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-budget.md) for the provider-specific parameters and requirements.

