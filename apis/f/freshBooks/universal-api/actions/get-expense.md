# FreshBooks: Get Expense

Retrieves an expense from FreshBooks for an account.

```
GET https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-expense?connectionId=$CONNECTION_ID&accountId=string&expenseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "expenseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-expense?${params}`, {
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
| `accountId` | string | yes | FreshBooks accounting account ID. |
| `expenseId` | string | yes | FreshBooks expense ID. |

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

Through the native FreshBooks API, this operation is `GET /accounting/account/:accountId/expenses/expenses/:expenseId` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expense.md) for the provider-specific parameters and requirements.

