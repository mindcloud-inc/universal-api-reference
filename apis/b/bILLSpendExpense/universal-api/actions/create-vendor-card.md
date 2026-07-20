# BILL Spend & Expense: Create Vendor Card

Creates a new vendor card in BILL Spend & Expense.

```
POST https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-vendor-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-vendor-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "budgetId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/create-vendor-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
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
| `expirationDate` | string | no | User-generated expiration date in yyyy-MM-dd format. |
| `name` | string | yes | Card name. |
| `budgetId` | list | yes | BILL-generated ID or UUID of the budget assigned to the card. |
| `userId` | list | yes | BILL-generated ID or UUID of the user assigned to the card. |
| `shareBudgetFunds` | boolean | no | Set true to share all budget funds with the card. |
| `limit` | number | no | Card spend limit for the current budget period. Required unless share budget funds is enabled. |
| `recurringLimit` | number | no | Card spend limit for all future budget periods when the assigned budget is recurring. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "budgetId": "string",
      "budgetUuid": "string",
      "createdTime": "string",
      "currentPeriod": {
        "limit": 1,
        "spent": 1
      },
      "id": "string",
      "lastFour": "string",
      "name": "Ava Chen",
      "recurring": true,
      "recurringLimit": 1,
      "shareBudgetFunds": true,
      "status": "string",
      "type": "string",
      "updatedTime": "string",
      "userId": "string",
      "userUuid": "string",
      "uuid": "string",
      "validThru": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budgetId` | string |  |
| `budgetUuid` | string |  |
| `createdTime` | string |  |
| `currentPeriod.limit` | number |  |
| `currentPeriod.spent` | number |  |
| `id` | string |  |
| `lastFour` | string |  |
| `name` | string |  |
| `recurring` | boolean |  |
| `recurringLimit` | number |  |
| `shareBudgetFunds` | boolean |  |
| `status` | string |  |
| `type` | string |  |
| `updatedTime` | string |  |
| `userId` | string |  |
| `userUuid` | string |  |
| `uuid` | string |  |
| `validThru` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `POST spend/cards` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-card.md) for the provider-specific parameters and requirements.

