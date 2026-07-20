# FreshBooks: Create Expense

Creates a new expense in FreshBooks for an account.

```
POST https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "expense.amount.amount": "string",
  "expense.amount.code": "string",
  "expense.categoryid": 1,
  "expense.date": "string",
  "expense.staffid": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "expense.amount.amount": "string",
    "expense.amount.code": "string",
    "expense.categoryid": 1,
    "expense.date": "string",
    "expense.staffid": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | FreshBooks accounting account ID. |
| `expense.amount.amount` | string | yes | Expense amount value. |
| `expense.amount.code` | string | yes | ISO currency code. |
| `expense.categoryid` | number | yes | FreshBooks expense category ID. |
| `expense.date` | string | yes | Expense date in YYYY-MM-DD format. |
| `expense.staffid` | number | yes | FreshBooks staff ID. |
| `expense.notes` | string | no | Expense memo text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingSystemid": "string",
      "amount": {},
      "billable": true,
      "categoryid": 1,
      "clientid": 1,
      "date": "string",
      "expenseid": 1,
      "hasReceipt": true,
      "id": 1,
      "invoiceid": 1,
      "isCogs": true,
      "markupPercent": "string",
      "notes": "string",
      "projectid": 1,
      "staffid": 1,
      "status": 1,
      "updated": "string",
      "visState": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingSystemid` | string |  |
| `amount` | object |  |
| `billable` | boolean |  |
| `categoryid` | number |  |
| `clientid` | number |  |
| `date` | string |  |
| `expenseid` | number |  |
| `hasReceipt` | boolean |  |
| `id` | number |  |
| `invoiceid` | number |  |
| `isCogs` | boolean |  |
| `markupPercent` | string |  |
| `notes` | string |  |
| `projectid` | number |  |
| `staffid` | number |  |
| `status` | number |  |
| `updated` | string |  |
| `visState` | number |  |

## Native endpoint

Through the native FreshBooks API, this operation is `POST /accounting/account/:accountId/expenses/expenses` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

