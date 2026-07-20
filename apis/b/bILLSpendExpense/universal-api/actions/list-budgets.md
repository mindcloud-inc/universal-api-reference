# BILL Spend & Expense: List Budgets

Retrieves budgets from BILL Spend & Expense.

```
GET https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-budgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-budgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-budgets?${params}`, {
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
| `filters` | string | no | Filter expression documented by BILL for this list endpoint. |
| `max` | string | no | Maximum number of results to return. |
| `nextPage` | string | no | Next page token returned by the previous list response. |
| `prevPage` | string | no | Previous page token returned by the previous list response. |
| `sort` | string | no | Sort expression documented by BILL for this list endpoint. |

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
        "overspendBuffer": 1,
        "spent": {
          "cleared": 1,
          "pending": 1,
          "total": 1
        },
        "startDate": "string"
      },
      "default": true,
      "expirationDate": "string",
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
| `currentPeriod.overspendBuffer` | number |  |
| `currentPeriod.spent.cleared` | number |  |
| `currentPeriod.spent.pending` | number |  |
| `currentPeriod.spent.total` | number |  |
| `currentPeriod.startDate` | string |  |
| `default` | boolean |  |
| `expirationDate` | string |  |
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

Through the native BILL Spend & Expense API, this operation is `GET spend/budgets` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-budgets.md) for the provider-specific parameters and requirements.

