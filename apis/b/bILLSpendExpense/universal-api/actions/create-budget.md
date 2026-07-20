# BILL Spend & Expense: Create Budget

Creates a new budget in BILL Spend & Expense.

```
POST https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "owners[]": [
    "string"
  ],
  "recurringInterval": "DAILY",
  "limit": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-budget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "owners[]": ["string"],
    "recurringInterval": "DAILY",
    "limit": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Budget description. |
| `name` | string | yes | Budget name. |
| `owners[]` | array<string> | yes | List of BILL-generated user IDs or UUIDs of budget owners. You must specify at least one budget owner. |
| `recurringInterval` | list | yes | Interval after which the budget is reset. One of: `DAILY`, `MONTHLY`, `NONE`, `QUARTERLY`, `WEEKLY`, `YEARLY`. |
| `limit` | number | yes | Spend limit for the initial budget period. Required unless limitless overspend is enabled. |
| `recurringLimit` | number | no | Spend limit for all future budget periods. Required when recurring interval is not NONE. |

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

Through the native BILL Spend & Expense API, this operation is `POST spend/budgets` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-budget.md) for the provider-specific parameters and requirements.

