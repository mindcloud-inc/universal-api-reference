# BILL Spend & Expense: List Cards

Retrieves vendor cards from BILL Spend & Expense.

```
GET https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-cards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-cards?${params}`, {
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
      "budgetId": "string",
      "budgetUuid": "string",
      "createdTime": "string",
      "currentPeriod": {
        "limit": 1,
        "spent": 1
      },
      "expirationDate": "string",
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
| `expirationDate` | string |  |
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

Through the native BILL Spend & Expense API, this operation is `GET spend/cards` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cards.md) for the provider-specific parameters and requirements.

